#!ansible-assign1
pipeline {
		agent {
			label {
				label "built-in"
			}
		}
		stages {
			stage ("cleaning workspace") {
				steps {
					cleanWs ()
				}
			}
			stage ("code checkout from scm") {
				steps {
					checkout scm
				}
			}
			stage ("installing httpd on hosts") {
				steps {
					sh 'ansible all -m yum -a "name=httpd state=installed" '
				}
			}
		}
}
