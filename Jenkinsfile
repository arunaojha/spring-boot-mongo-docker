node{
     
    stage('SCM Checkout'){
        git credentialsId: 'gittoken', url: 'https://github.com/arunaojha/spring-boot-mongo-docker.git'
    }
    
    stage(" Maven Clean Package"){
      def mavenHome =  tool name: "maven3.9.9", type: "maven"
      def mavenCMD = "${mavenHome}/bin/mvn"
      sh "${mavenCMD} clean package"
      
    } 
    
    /**
    stage('Build Docker Image'){
        sh 'docker build -t dockerhandson/spring-boot-mongo .'
    }
    
    stage('Push Docker Image'){
        withCredentials([string(credentialsId: 'DOKCER_HUB_PASSWORD', variable: 'DOKCER_HUB_PASSWORD')]) {
          sh "docker login -u dockerhandson -p ${DOKCER_HUB_PASSWORD}"
        }
        sh 'docker push dockerhandson/spring-boot-mongo'
     }
     
     stage("Deploy To Kuberates Cluster"){
       kubernetesDeploy(
         configs: 'springBootMongo.yml', 
         kubeconfigId: 'KUBERNATES_CONFIG',
         enableConfigSubstitution: true
        )
     }
	 
	  
      stage("Deploy To Kuberates Cluster"){
        sh 'kubectl apply -f springBootMongo.yml'
      } **/
     
}
