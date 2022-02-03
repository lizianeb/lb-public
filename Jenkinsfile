def ipvaFileFolder = "https://github.com/lizianeb/lb.git"

pipeline{
    agent any

    stages {
        stage('Criação usuário cognito'){
            steps {
                script {
                    dir (ipvaFileFolder){
                        if(fileExists("teste_file.csv")) {
                            echo 'Arquivo teste_file.csv não encontrado.'
                            
                            readFile("teste_file.csv").split('\n').each { line, count ->
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
