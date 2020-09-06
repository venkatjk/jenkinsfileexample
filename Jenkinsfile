pipeline {
	agent none
	//agent {
		//node {
			//label 'slave1'
		//}
	//}
	
	options {
		timestamps()
		}
		
	stages {
		stage("Paralle"){
			agent any
			steps {
				parallel (
				 "Taskone" : {
					 echo "from parallel...1"
				 },
				 "Tasktwo" : {
					 echo "from parallel......2"
				 }
				)
			}
			
		}
	}
	 post { 
        failure { 
            echo 'I will always say Hello again!'
        }
    }
}