node {
	stage 'Checkout'
		checkout scm

	stage 'Build'
		bat dotnet restore MvcMovie.csproj'
		bat "\"${tool 'MSBuild'}\" MvcMovie.csproj /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"

	stage 'Archive'
		archive 'ProjectName/bin/Release/**'

}


