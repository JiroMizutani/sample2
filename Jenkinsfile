node {
  stage('codebuild') {
    awsCodeBuild(
      projectName: 'sandbox',
      region: 'ap-northeast-1',
      sourceControlType: 'project',
      sourceVersion: env.BRANCH_NAME,
      // CodeBuild�Ƀu�����`�������ϐ��œn������
      envVariables: "[{BRANCH_NAME,${env.BRANCH_NAME}}]",
    )
  }
}