stage("Win32 / Win64") {
    node('windows') {
        checkout scm
        bat 'git submodule update --init'
        powershell '.\\Build.ps1'
        stash includes: 'dist/**', name: 'windows'
    }
}