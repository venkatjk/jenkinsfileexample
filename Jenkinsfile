pipeline {
	agent any
	stages {
		stage("Paralle"){
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
			exit 1
		}
	}
	 post { 
        failure { 
            echo 'I will always say Hello again!'
        }
    }
}