node('DOTNETCORE'){
	stage('SCM'){
		checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/msfs-junin/JenkinsDocker']]])
	}
	stage('Construir'){
		try{
		  //sh '/usr/bin/dotnet build ConsoleApp1'
		  whereis dotnet
		}finally{
		//archiveArtifacts artifacts: 'ConsoleApp1/*.*'
		}
	}
	stage('Correr tests'){
		echo 'Execute unit tests'
	}
	stage('Empaquetar'){
		echo 'Zip it up'
	}
	stage('Desplegar'){
		echo 'Push to deployment'
	}
	stage('Archivar'){
		//archiveArtifacts artifacts: 'ConsoleApp1/*.*'
	}
}
