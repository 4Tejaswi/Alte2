pipeline {
	agent any
	stages {
		stage ('Build') {
			steps {
				echo 'Print Step 1 is Build'
			}
		}
		stage ('Input') {
			steps {
				input ('Yes/No')
			}
		}
		stage ('Condition') {
			when {
				not {
					branch 'master'
				}
			}
			steps {
				echo 'Print Step 3 is Condition'
			}
		}
		stage ('InParallel') {
			parallel {
				stage ( 'Test 1') {
					steps {
						echo 'Print Step 4.1 is In Prallel Test1'
					}
				}
				stage ( 'Test 2') {
					steps {
						echo 'Print Step 4.2 is In Prallel Test2'
					}
				}
				stage ( 'Print step' ) {
					steps {
				        	echo 'Print Step 4.3 final'
					}
				}
			}
		}
	}
}

