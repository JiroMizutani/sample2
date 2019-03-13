node {
  stage('codebuild') {
    awsCodeBuild(
      projectName: 'sandbox',
      region: 'ap-northeast-1',
      sourceControlType: 'project',
      sourceVersion: env.BRANCH_NAME,
      // CodeBuild‚Éƒuƒ‰ƒ“ƒ`–¼‚ğŠÂ‹«•Ï”‚Å“n‚·‚½‚ß
      envVariables: "[{BRANCH_NAME,${env.BRANCH_NAME}}]",
    )
  }
}