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
		}
	}
	 post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}