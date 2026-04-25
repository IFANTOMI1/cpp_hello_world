pipeline{
    agent any
    stages{
        stage('Print Info'){
            steps{
                sh 'echo "Branch: main"'
                sh 'echo "Hash: 3e8e19b4f26f10c19cf66c4979dce6565a22a9b9"'
                sh 'echo "g++ version: Apple clang version 17.0.0 (clang-1700.6.3.2)"'
Target: arm64-apple-darwin24.6.0
Thread model: posix
InstalledDir: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin
            }
        }
        stage('Build Executable file'){
            steps{
                // Компилируем main.cpp и сохраняем результат в файл main
                sh 'g++ main.cpp -o main'
            }
        }
        stage('Application Launch Test'){
            steps{
                // Запускаем исполняемый файл main из текущего каталога
                sh './main'
            }
        }
    }
}
