node('Group1') {
	stage('SCM') {
		echo "To clone from Github"
		git 'https://github.com/vidyasagardevops20/game-of-life.git'
	}
	stage('BUILD') {
		echo "This is BUILD Section"
		sh 'mvn package'
	}
	stage('PostBUILD') {
		echo "This is Post Build Action"
		junit 'gameoflife-web/target/surefire-reports/*.xml'
	}
	stage('ARCHIVE ARIFACTS') {
		echo "Archiveing the Artifacts here"
		archive 'gameoflife-web/target/*.war'
	}
}
