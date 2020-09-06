pipeline {
	agent any
	stages {
		stage("Paralled"){
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
}