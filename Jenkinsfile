pipeline  {
	agent any
	environment {
		NEW_VERSION = "1.3.0"
	}
	parameters {
		choice(name: 'VERSION', choices:['1.1.0', '1.2.0', '1.3.0'], description:'')
		booleanParam(name: "executeTest", defaultValue:true, description:'')
	}
	stages {
		stage("build") {
			steps {
				echo "bulding the application."
				echo "bulding the ${NEW_VERSION}."
			}
		}
		stage("test") {
			when {
				expression {
					param.executeTest == true
				}
			}
			steps {
				echo "testing the application."
			}
		}
		stage("deploy") {
			steps {
				echo "deploying the version ${VERSION}."
			}
		}

	}
}