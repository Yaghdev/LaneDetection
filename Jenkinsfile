pipeline  {
	agent any
	environment {
		NEW_VERSION = "1.3.0"
	}
	stages {
		stage("build") {
			steps {
				echo "bulding the application."
				echo "bulding the ${NEW_VERSION}."
			}
		}
		stage("test") {
			steps {
				echo "testing the application."
			}
		}
		stage("deploy") {
			steps {
				echo "deploying the application."
			}
		}

	}
}