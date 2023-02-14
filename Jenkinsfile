pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'sudo apt-get update && sudo apt-get install -y build-essential'
                
                // Compiling the C++ program
                sh 'g++ -o ./Server/server.cpp'
                sh 'g++ -o ./Client/client.cpp'
            }
        }
//         stage('Push Release') {
//         steps {
//           script {
//             // Create a GitHub release
//             def github = github()
//             def release = github.createRelease(
//                 tagName: 'v2.0.0',
//                 name: 'My Program Release', 
//                 body: 'Release Notes' 
//             )
            
//             // Uploading the built artifact to the release
//             def uploadUrl = release.uploadUrl
//             def fileName = 'myprogram.zip' // Set the name of the artifact file
//             def file = new File(fileName)
//             def fileSize = file.length()
            
//             sh "curl -H 'Authorization: token ${github.accessToken}' -H 'Content-Type: application/zip' --data-binary @${fileName} -X POST '${uploadUrl}?name=${fileName}&size=${fileSize}'"
//         }
//     }
// }

    }
}
