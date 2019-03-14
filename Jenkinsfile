node {
  stage('codebuild') {
    awsCodeBuild(
      projectName: 'jenkins-build',
      region: 'ap-northeast-1',
      sourceControlType: 'jenkins',
      sourceVersion: env.BRANCH_NAME,
      credentialsType: 'keys',
      // CodeBuildにブランチ名を環境変数で渡すため
      envVariables: "[{BRANCH_NAME,${env.BRANCH_NAME}}]",
    )
  }
}