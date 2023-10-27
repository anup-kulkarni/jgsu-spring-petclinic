def label = "mypod-${UUID.randomUUID().toString()}"
trunkBranch = "main";
releaseBranch = 'release/candidate';
featureBranch = 'featurebranch'
List<String> imageTagsToPush = [];

echo "!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!";

echo env.BRANCH_NAME;
def sanitizedBranchName = ""
      if(env.BRANCH_NAME == releaseBranch || env.BRANCH_NAME == trunkBranch) {
        sanitizedBranchName = env.BRANCH_NAME.replaceAll("feature/", "").replaceAll("bugfix/", "").replaceAll("hotfix/", "").toLowerCase();
      } else {
        sanitizedBranchName = featureBranch;
      }

echo sanitizedBranchName
