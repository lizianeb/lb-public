def ipvaFileFolder = "https://github.com/lizianeb/lb.git"

pipeline{
    stages {
        stage('Criação usuário cognito'){
            steps {
                script {
                    dir (ipvaFileFolder){
                        if(fileExists(ipva.csv)) {
                            readFile("arquivo.csv").split('\n').each { line, count ->
                            def fields = line.split
                            for(String item: fields) {
                                println item
                                print 'linha' + count
                            }
                        } 
                        }
                    }      
                }
            }
        }
    }
}
