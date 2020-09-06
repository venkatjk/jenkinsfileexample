pipeline {
	agent none
	//agent any
	//agent {
		//node {
			//label 'slave1'
		//}
	//}
	
	options {
		timestamps()
		}
		
		environment {
			NAME = 'VENKAT'
			CITY = 'NCL'
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
		stage("Build") {
			agent {
				node {
					label 'slave1'
				}
			}
			steps {
				echo 'From build stage'
				sh 'printenv'
				}
		}
	}
	 post { 
        failure { 
            echo 'I will always say Hello again!'
        }
    }
}