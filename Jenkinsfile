def label = "mypod-${UUID.randomUUID().toString()}"
trunkBranch = "master";
releaseBranch = 'release/candidate';
List<String> imageTagsToPush = [];

echo "!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!";

echo env.BRANCH_NAME;

      if(env.BRANCH_NAME == releaseBranch || env.BRANCH_NAME == trunkBranch) {
        def sanitizedBranchName = env.BRANCH_NAME.replaceAll("feature/", "").replaceAll("bugfix/", "").replaceAll("hotfix/", "").toLowerCase();
      } else {
        def sanitizedBranchName = featureBranch;
      }

echo sanitizedBranchName
