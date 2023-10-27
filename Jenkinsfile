def label = "mypod-${UUID.randomUUID().toString()}"
trunkBranch = "master";
releaseBranch = 'release/candidate';
List<String> imageTagsToPush = [];

echo "!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!";

echo env.BRANCH_NAME;

properties([
  parameters([
    choice(name: 'SKIP_UNIT_TESTS', choices:['No', 'Yes']),
  ])
])
