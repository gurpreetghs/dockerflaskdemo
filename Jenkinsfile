stage('Docker Nexus Auth'){
sh 'docker login -u admin -p 123 44.201.118.101:9001'
}

stage('Push Docker Images to Nexus Registry'){
sh 'docker push http://54.211.71.95:8081/repository/demoimg//DepImg}'
sh 'docker rmi $(docker images --filter=reference="http://54.211.71.95:8081/repository/demoimg//DepImg*" -q)'
sh 'docker logout http://54.211.71.95:8081/repository/demoimg//DepImg'
}
