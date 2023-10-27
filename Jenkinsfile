def label = "mypod-${UUID.randomUUID().toString()}"
trunkBranch = "master";
releaseBranch = 'release/candidate';
List<String> imageTagsToPush = []



// Initializing Nodejs
{
  properties([
    parameters([
      choice(name: 'OVERRIDE_AND_DEPLOY', choices: ['false', 'true']),
      [
        $class: "ChoiceParameter",
        choiceType: 'PT_SINGLE_SELECT',
        description: "Select the environment to deploy",
        name: "Select the environment to deploy",
        script: [
          $class: 'GroovyScript',
          script: [
            classpath: [],
            sandbox: false,            
            script: '''
                    if (env.BRANCH_NAME == releaseBranch) {
                      return ["int: int"]
                    } else if (env.BRANCH_NAME == trunkBranch) {
                      return ["dev: dev", "deva: deva"]
                    } else {
                      return ["deva: deva"]
                    }             
            '''
          ]
        ]
      ]
    ])
  ])
}
