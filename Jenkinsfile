def label = "mypod-${UUID.randomUUID().toString()}"
trunkBranch = "master";
releaseBranch = 'release/candidate';
List<String> imageTagsToPush = []

echo "!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!";

{
  properties([
    parameters([
      choice(name: 'OVERRIDE_AND_DEPLOY', choices: ['false', 'true']),
      
    ])
  ])


