Started by GitHub push by D-Mwanth
Obtained Jenkinsfile from git https://github.com/D-Mwanth/microservices-build-pipeline
Loading library ci-library@main
Attempting to resolve main from remote references...
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
 > git ls-remote -h -- https://github.com/D-Mwanth/microservices-build-pipeline # timeout=10
Found match: refs/heads/main revision 41dbfceafe950081224dafe54589ec1f35aee9e3
Selected Git installation does not exist. Using Default
The recommended git tool is: NONE
No credentials specified
 > git rev-parse --resolve-git-dir /var/lib/jenkins/workspace/microservices-build@libs/234dc070aeabf2f6fd2cc25edb7cf070e38fbb9da90f665b14113b67e5d42a5b/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/D-Mwanth/microservices-build-pipeline # timeout=10
Fetching without tags
Fetching upstream changes from https://github.com/D-Mwanth/microservices-build-pipeline
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
 > git fetch --no-tags --force --progress -- https://github.com/D-Mwanth/microservices-build-pipeline +refs/heads/*:refs/remotes/origin/* # timeout=10
Checking out Revision 41dbfceafe950081224dafe54589ec1f35aee9e3 (main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 41dbfceafe950081224dafe54589ec1f35aee9e3 # timeout=10
Commit message: "Updated `buildOrReBuildImage.groovy` to remove dangling images"
 > git rev-list --no-walk 41dbfceafe950081224dafe54589ec1f35aee9e3 # timeout=10
[Pipeline] Start of Pipeline
[Pipeline] node
Running on Jenkins-Agent in /home/ubuntu/workspace/microservices-build
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
Selected Git installation does not exist. Using Default
The recommended git tool is: NONE
No credentials specified
Cloning the remote Git repository
Avoid second fetch
Checking out Revision 41dbfceafe950081224dafe54589ec1f35aee9e3 (refs/remotes/origin/main)
Commit message: "Updated `buildOrReBuildImage.groovy` to remove dangling images"
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] withEnv
[Pipeline] {
Cloning repository https://github.com/D-Mwanth/microservices-build-pipeline
 > git init /home/ubuntu/workspace/microservices-build # timeout=10
Fetching upstream changes from https://github.com/D-Mwanth/microservices-build-pipeline
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
 > git fetch --tags --force --progress -- https://github.com/D-Mwanth/microservices-build-pipeline +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git config remote.origin.url https://github.com/D-Mwanth/microservices-build-pipeline # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 41dbfceafe950081224dafe54589ec1f35aee9e3 # timeout=10
[Pipeline] stage
[Pipeline] { (Cleanup Workspace)
[Pipeline] cleanWs
[WS-CLEANUP] Deleting project workspace...
[WS-CLEANUP] Deferred wipeout is used...
[WS-CLEANUP] done
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Checkout Microservices & K8s Manifests)
[Pipeline] script
[Pipeline] {
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app
[Pipeline] {
[Pipeline] git
The recommended git tool is: NONE
No credentials specified
Cloning the remote Git repository
Avoid second fetch
Checking out Revision a1bbf5a1210a544f7ce3321a4414deb2c7b2be9a (refs/remotes/origin/main)
Cloning repository https://github.com/D-Mwanth/microservices-app.git
 > git init /home/ubuntu/workspace/microservices-build/microservices-app # timeout=10
Fetching upstream changes from https://github.com/D-Mwanth/microservices-app.git
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
 > git fetch --tags --force --progress -- https://github.com/D-Mwanth/microservices-app.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git config remote.origin.url https://github.com/D-Mwanth/microservices-app.git # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
 > git config core.sparsecheckout # timeout=10
 > git checkout -f a1bbf5a1210a544f7ce3321a4414deb2c7b2be9a # timeout=10
 > git branch -a -v --no-abbrev # timeout=10
 > git checkout -b main a1bbf5a1210a544f7ce3321a4414deb2c7b2be9a # timeout=10
Commit message: "Updated README.md file of adservice, checkoutservice, shippingservice"
 > git rev-list --no-walk a136e140a2ce54a1dfbe8182fb996785d77ff6cf # timeout=10
[Pipeline] }
[Pipeline] // dir
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/kubernetes-manifests
[Pipeline] {
[Pipeline] git
The recommended git tool is: NONE
No credentials specified
Cloning the remote Git repository
Avoid second fetch
Checking out Revision 073329f5ed4b7202df562fc3bbff231a50d1142c (refs/remotes/origin/main)
Commit message: "Updated Deployment Manifest-Build 1"
Cloning repository https://github.com/D-Mwanth/kubernetes-manifests.git
 > git init /home/ubuntu/workspace/microservices-build/kubernetes-manifests # timeout=10
Fetching upstream changes from https://github.com/D-Mwanth/kubernetes-manifests.git
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
 > git fetch --tags --force --progress -- https://github.com/D-Mwanth/kubernetes-manifests.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git config remote.origin.url https://github.com/D-Mwanth/kubernetes-manifests.git # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 073329f5ed4b7202df562fc3bbff231a50d1142c # timeout=10
 > git branch -a -v --no-abbrev # timeout=10
 > git checkout -b main 073329f5ed4b7202df562fc3bbff231a50d1142c # timeout=10
 > git rev-list --no-walk 65bcf89214e72b5f294bc4c98685c600d92691b0 # timeout=10
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Determine Services to Build)
[Pipeline] script
[Pipeline] {
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app
[Pipeline] {
[Pipeline] sh
+ git diff --name-status HEAD~1
+ grep src
+ cut -d / -f 2
+ + sort
grep -v ^D
+ grep -v /.gitignore
+ uniq
+ tr \n  
[Pipeline] }
[Pipeline] // dir
[Pipeline] echo
Services to Build: [adservice, checkoutservice, shippingservice]
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Build or Rebuild Services)
[Pipeline] script
[Pipeline] {
[Pipeline] sh
+ mkdir -p /home/ubuntu/track/microservices-build
[Pipeline] sh
+ touch /home/ubuntu/track/microservices-build/existingServices.txt
[Pipeline] sh
+ chmod -R 777 /home/ubuntu/workspace/microservices-build/kubernetes-manifests
[Pipeline] script
[Pipeline] {
[Pipeline] readFile
[Pipeline] }
[Pipeline] // script
[Pipeline] echo
[adservice, checkoutservice, shippingservice]
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Rebuilding and Pushing adservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/5b6ef892-55fe-44c0-8f01-b6689a57a399/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ grep image: mwanthi/adservice:[^[:space:]]* /home/ubuntu/workspace/microservices-build/kubernetes-manifests/adservice/adservice.yaml
+ awk {gsub(/^v/, ""); print}
+ awk -F : {print $3}
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app/src/adservice
[Pipeline] {
[Pipeline] sh
+ docker build --no-cache -t mwanthi/adservice .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  97.28kB

Step 1/14 : FROM eclipse-temurin:21@sha256:e538e34d1df871c9b7da571582cdc49538f1eaee1dacbfb317a3e7f54abeebae AS builder
docker.io/library/eclipse-temurin:21@sha256:e538e34d1df871c9b7da571582cdc49538f1eaee1dacbfb317a3e7f54abeebae: Pulling from library/eclipse-temurin
32b824d45c61: Pulling fs layer
fe18bb7e114f: Pulling fs layer
581ebfe08d3f: Pulling fs layer
7c7bdd063feb: Pulling fs layer
28f1e2918031: Pulling fs layer
7c7bdd063feb: Waiting
28f1e2918031: Waiting
32b824d45c61: Verifying Checksum
32b824d45c61: Download complete
fe18bb7e114f: Verifying Checksum
fe18bb7e114f: Download complete
7c7bdd063feb: Verifying Checksum
7c7bdd063feb: Download complete
28f1e2918031: Verifying Checksum
28f1e2918031: Download complete
32b824d45c61: Pull complete
581ebfe08d3f: Verifying Checksum
581ebfe08d3f: Download complete
fe18bb7e114f: Pull complete
581ebfe08d3f: Pull complete
7c7bdd063feb: Pull complete
28f1e2918031: Pull complete
Digest: sha256:e538e34d1df871c9b7da571582cdc49538f1eaee1dacbfb317a3e7f54abeebae
Status: Downloaded newer image for eclipse-temurin:21@sha256:e538e34d1df871c9b7da571582cdc49538f1eaee1dacbfb317a3e7f54abeebae
 ---> 8f2c4d2db181
Step 2/14 : WORKDIR /app
 ---> Running in a003f57a79f4
Removing intermediate container a003f57a79f4
 ---> f96ed16c5dd7
Step 3/14 : COPY ["build.gradle", "gradlew", "./"]
 ---> 3ff9454b35b0
Step 4/14 : COPY gradle gradle
 ---> 8b290e4f86c0
Step 5/14 : RUN chmod +x gradlew
 ---> Running in 570e700b018d
Removing intermediate container 570e700b018d
 ---> 0f97d49a08fb
Step 6/14 : RUN ./gradlew downloadRepos
 ---> Running in 46e18dba6437
Downloading https://services.gradle.org/distributions/gradle-8.10.2-bin.zip
.............10%.............20%.............30%.............40%.............50%.............60%.............70%.............80%.............90%.............100%

Welcome to Gradle 8.10.2!

Here are the highlights of this release:
 - Support for Java 23
 - Faster configuration cache
 - Better configuration cache reports

For more details see https://docs.gradle.org/8.10.2/release-notes.html

Starting a Gradle Daemon (subsequent builds will be faster)
> Task :downloadRepos

Deprecated Gradle features were used in this build, making it incompatible with Gradle 9.0.

You can use '--warning-mode all' to show the individual deprecation warnings and determine if they come from your own scripts or plugins.

For more on this, please refer to https://docs.gradle.org/8.10.2/userguide/command_line_interface.html#sec:command_line_warnings in the Gradle documentation.

BUILD SUCCESSFUL in 27s
1 actionable task: 1 executed
Removing intermediate container 46e18dba6437
 ---> 6c632b3d526b
Step 7/14 : COPY . .
 ---> e28f2f0dbad6
Step 8/14 : RUN chmod +x gradlew
 ---> Running in 2d04b3cc6fd7
Removing intermediate container 2d04b3cc6fd7
 ---> b3a3faf5eec6
Step 9/14 : RUN ./gradlew installDist
 ---> Running in ae512c75a57e
Starting a Gradle Daemon, 1 incompatible and 1 stopped Daemons could not be reused, use --status for details
> Task :extractIncludeProto
> Task :extractProto
> Task :generateProto

> Task :compileJava
[91mNote: /app/src/main/java/hipstershop/AdService.java uses or overrides a deprecated API.[0m[91m
[0m[91mNote: Recompile with -Xlint:deprecation for details.[0m[91m
[0m
> Task :processResources
> Task :classes
> Task :jar
> Task :adService
> Task :adServiceClient
> Task :startScripts SKIPPED
> Task :installDist

Deprecated Gradle features were used in this build, making it incompatible with Gradle 9.0.

You can use '--warning-mode all' to show the individual deprecation warnings and determine if they come from your own scripts or plugins.

For more on this, please refer to https://docs.gradle.org/8.10.2/userguide/command_line_interface.html#sec:command_line_warnings in the Gradle documentation.

BUILD SUCCESSFUL in 35s
9 actionable tasks: 9 executed
Removing intermediate container ae512c75a57e
 ---> a48e74fa880f
Step 10/14 : FROM eclipse-temurin:21.0.4_7-jre-alpine@sha256:8cc1202a100e72f6e91bf05ab274b373a5def789ab6d9e3e293a61236662ac27
docker.io/library/eclipse-temurin:21.0.4_7-jre-alpine@sha256:8cc1202a100e72f6e91bf05ab274b373a5def789ab6d9e3e293a61236662ac27: Pulling from library/eclipse-temurin
43c4264eed91: Already exists
4fb0eeeb44ea: Pulling fs layer
6be5feca48e3: Pulling fs layer
0efe887b0486: Pulling fs layer
c4d7b64b67a4: Pulling fs layer
c4d7b64b67a4: Waiting
0efe887b0486: Verifying Checksum
0efe887b0486: Download complete
4fb0eeeb44ea: Verifying Checksum
4fb0eeeb44ea: Download complete
c4d7b64b67a4: Verifying Checksum
c4d7b64b67a4: Download complete
4fb0eeeb44ea: Pull complete
6be5feca48e3: Verifying Checksum
6be5feca48e3: Download complete
6be5feca48e3: Pull complete
0efe887b0486: Pull complete
c4d7b64b67a4: Pull complete
Digest: sha256:8cc1202a100e72f6e91bf05ab274b373a5def789ab6d9e3e293a61236662ac27
Status: Downloaded newer image for eclipse-temurin:21.0.4_7-jre-alpine@sha256:8cc1202a100e72f6e91bf05ab274b373a5def789ab6d9e3e293a61236662ac27
 ---> 29ce5002d122
Step 11/14 : WORKDIR /app
 ---> Running in 82da158fb7da
Removing intermediate container 82da158fb7da
 ---> d283640a7816
Step 12/14 : COPY --from=builder /app .
 ---> 870edafbe6fb
Step 13/14 : EXPOSE 9555
 ---> Running in a4ba2b91a748
Removing intermediate container a4ba2b91a748
 ---> a337cc4d721c
Step 14/14 : ENTRYPOINT ["/app/build/install/hipstershop/bin/AdService"]
 ---> Running in e27a66648942
Removing intermediate container e27a66648942
 ---> 0e2a09457ac4
Successfully built 0e2a09457ac4
Successfully tagged mwanthi/adservice:latest
[Pipeline] sh
+ docker tag mwanthi/adservice mwanthi/adservice:v0.0.2
[Pipeline] sh
+ docker push mwanthi/adservice:v0.0.2
The push refers to repository [docker.io/mwanthi/adservice]
36a65f7d8104: Preparing
5b0629a7db82: Preparing
71e8cc6fa9c8: Preparing
44a76360121e: Preparing
13407d63b650: Preparing
01d3f5d5a6c9: Preparing
63ca1fbb43ae: Preparing
63ca1fbb43ae: Waiting
01d3f5d5a6c9: Waiting
13407d63b650: Layer already exists
44a76360121e: Layer already exists
71e8cc6fa9c8: Layer already exists
01d3f5d5a6c9: Layer already exists
63ca1fbb43ae: Layer already exists
5b0629a7db82: Pushed
36a65f7d8104: Pushed
v0.0.2: digest: sha256:d9a1cc5492ce7b8ea4204e317a331197bcbbaf0e0085941405527366cdf35438 size: 1784
[Pipeline] sh
+ docker push mwanthi/adservice:latest
The push refers to repository [docker.io/mwanthi/adservice]
36a65f7d8104: Preparing
5b0629a7db82: Preparing
71e8cc6fa9c8: Preparing
44a76360121e: Preparing
13407d63b650: Preparing
01d3f5d5a6c9: Preparing
63ca1fbb43ae: Preparing
63ca1fbb43ae: Waiting
01d3f5d5a6c9: Waiting
13407d63b650: Layer already exists
36a65f7d8104: Layer already exists
71e8cc6fa9c8: Layer already exists
5b0629a7db82: Layer already exists
44a76360121e: Layer already exists
01d3f5d5a6c9: Layer already exists
63ca1fbb43ae: Layer already exists
latest: digest: sha256:d9a1cc5492ce7b8ea4204e317a331197bcbbaf0e0085941405527366cdf35438 size: 1784
[Pipeline] sh
+ sed -i  -e s|mwanthi/adservice:v0.0.1|mwanthi/adservice:v0.0.2|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/adservice/adservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/adservice:latest
Untagged: mwanthi/adservice:latest
[Pipeline] sh
+ docker rmi mwanthi/adservice:v0.0.2
Untagged: mwanthi/adservice:v0.0.2
Untagged: mwanthi/adservice@sha256:d9a1cc5492ce7b8ea4204e317a331197bcbbaf0e0085941405527366cdf35438
Deleted: sha256:0e2a09457ac475dd512bd914792e7e1c3aeca0ebc59d133e194d7ab476d37389
Deleted: sha256:a337cc4d721cccc395999505f969bcd8cfbd353f6a12e9bd589d2a01686a3d85
Deleted: sha256:870edafbe6fb09f1f1808b183617b47c3c5f78fbeb44cd3aeffb436c7265d49d
Deleted: sha256:c9fd69ba1466df24611ed67c5534d3a6021de7e897919f9fa18cb01596310a48
Deleted: sha256:d283640a7816ef5f1cb243f38ecf937419d23899b5e40b5ce21aa2464358ce8e
Deleted: sha256:443862d8f3c17582c880d22cdcebe0699b012722d5fe29186dd185e682cc5348
[Pipeline] sh
+ docker image prune -f
Deleted Images:
deleted: sha256:a48e74fa880f6c5ce50b8cced890ef610e18d9d52459be7264684fc00dc04d36
deleted: sha256:bc98a7cdbb8dde99eee15c24a92e6527ba52e12748778d74302dafd42d10a84f
deleted: sha256:b3a3faf5eec6166efb758061e4a6d15ea64a7d7e96a398faa92238b631529161
deleted: sha256:84cf98dd67f084781d98711c4803054cffabef955f0cfeec692ab056a0478fe3
deleted: sha256:e28f2f0dbad62721515c824122059a106fe1da16777c98561975848640da177b
deleted: sha256:911bf02e38c99dcf2d67fe04309015d804abffc2e544dbf30c64c0d99fe05e7e
deleted: sha256:6c632b3d526be423968c8e959a4dcb7317877d28b5ab2127e0e4a505a8807deb
deleted: sha256:a852b45555dc1f1319078c63b89baef640dcc9f8f98d358460383ec9574934d9
deleted: sha256:0f97d49a08fb2c27c55a39bc9a7b8a04f671a62205c630779446a5a3ae6609b0
deleted: sha256:52e3bce27b425f56225153859c39a0d7314636d0d0c5c608fa817f0e9e3be9f6
deleted: sha256:8b290e4f86c076b36d7e63db61572a32aee57e4969728904420e527293efc39c
deleted: sha256:68a5b923ef3554071b2661eca2e07aa982a8db6447b74d5add0ddb37f4244c8f
deleted: sha256:3ff9454b35b0d9594443e0b01a98bd5da2042c6ef2ba1e89b53ea276418bb039
deleted: sha256:0f93a62d9eb4f0c74dccfd7673642a5fab82bad2aba2e9864c64f2d78176531c
deleted: sha256:f96ed16c5dd78b86f31d268f3291548207710af5662baa762d433c1fb9a2f919
deleted: sha256:eab3af854507e1827a36cf75f9d09c6f9ec4fff7fce1db3670be0116359d21ce
untagged: golang@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06
deleted: sha256:b5ada884192f173018fcb39688bd70545669ab105941231067ea5dbed4ac6914
deleted: sha256:2968ff6a64392cda70b3e2cb5d6e62723bfdc18fe68b46382c971bee002890a2
deleted: sha256:768a08d8d838830bce342fdf82d2051ad375b9a575cb6cb685f8841bc16f5ae2
deleted: sha256:7c37ab7540e48469f2843766943fb1f5b838efe35a1e500268f45f1b6ba88942
deleted: sha256:db287705205f639bdfff0f98a53c5b40608826ee5ab2b1180bcf22eec319953c
untagged: eclipse-temurin@sha256:8cc1202a100e72f6e91bf05ab274b373a5def789ab6d9e3e293a61236662ac27
deleted: sha256:29ce5002d122a67eb0e9e1889f04519886ef38baea0a9410138798e8d95ff6af
deleted: sha256:ce97291ed233db35a28773072a090d19c498336b3b3d2cc8b368957d9641bb6e
deleted: sha256:9da47462cb0d9f03cbf3a2ed03b764e239c6ea4a078aad49e8e005c75d083a86
deleted: sha256:f3752a5777d03e8e36ca44c11e15482b3c7433a2ca77ee0ef289348a9b4f9ab7
deleted: sha256:7dada8fb0e360803bb185862b64e2c6c0888266672bd22c268a713bd6fbd57ea
deleted: sha256:63ca1fbb43ae5034640e5e6cb3e083e05c290072c5366fcaa9d62435a4cced85

Total reclaimed space: 672.7MB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Rebuilding and Pushing checkoutservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/9fcb6e8e-423f-40b6-8371-c40f3b3c56d3/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ grep image: mwanthi/checkoutservice:[^[:space:]]* /home/ubuntu/workspace/microservices-build/kubernetes-manifests/checkoutservice/checkoutservice.yaml
+ awk -F : {print $3}
+ awk {gsub(/^v/, ""); print}
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app/src/checkoutservice
[Pipeline] {
[Pipeline] sh
+ docker build --no-cache -t mwanthi/checkoutservice .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  200.2kB

Step 1/13 : FROM golang:1.23.1-alpine@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06 AS builder
docker.io/library/golang:1.23.1-alpine@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06: Pulling from library/golang
43c4264eed91: Pulling fs layer
ab19dfae90ef: Pulling fs layer
e7bff916ab0c: Pulling fs layer
78cee99375e3: Pulling fs layer
4f4fb700ef54: Pulling fs layer
78cee99375e3: Waiting
4f4fb700ef54: Waiting
ab19dfae90ef: Verifying Checksum
ab19dfae90ef: Download complete
43c4264eed91: Verifying Checksum
43c4264eed91: Download complete
43c4264eed91: Pull complete
78cee99375e3: Verifying Checksum
78cee99375e3: Download complete
ab19dfae90ef: Pull complete
4f4fb700ef54: Verifying Checksum
4f4fb700ef54: Download complete
e7bff916ab0c: Verifying Checksum
e7bff916ab0c: Download complete
e7bff916ab0c: Pull complete
78cee99375e3: Pull complete
4f4fb700ef54: Pull complete
Digest: sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06
Status: Downloaded newer image for golang:1.23.1-alpine@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06
 ---> b5ada884192f
Step 2/13 : WORKDIR /src
 ---> Running in 86891633fa51
Removing intermediate container 86891633fa51
 ---> 304074a59a97
Step 3/13 : COPY go.mod go.sum ./
 ---> dee93d512d28
Step 4/13 : RUN go mod download
 ---> Running in e8ccb5bc83ae
Removing intermediate container e8ccb5bc83ae
 ---> 001cb48c5c47
Step 5/13 : COPY . .
 ---> 85258fe45a49
Step 6/13 : ARG SKAFFOLD_GO_GCFLAGS
 ---> Running in 62df576b5f0d
Removing intermediate container 62df576b5f0d
 ---> 8a3745cdef84
Step 7/13 : RUN CGO_ENABLED=0 GOOS=linux go build -gcflags="${SKAFFOLD_GO_GCFLAGS}" -o /checkoutservice .
 ---> Running in a456a8f3e290
Removing intermediate container a456a8f3e290
 ---> b3338a44dcda
Step 8/13 : FROM scratch
 ---> 
Step 9/13 : WORKDIR /src
 ---> Running in 77338c22cdf9
Removing intermediate container 77338c22cdf9
 ---> a0a70f67895f
Step 10/13 : COPY --from=builder /checkoutservice /src/checkoutservice
 ---> 938e14b393e9
Step 11/13 : ENV GOTRACEBACK=single
 ---> Running in ab1443414e1d
Removing intermediate container ab1443414e1d
 ---> 82dfdf1cda86
Step 12/13 : EXPOSE 5050
 ---> Running in 6fa8289764bf
Removing intermediate container 6fa8289764bf
 ---> b43b095f2999
Step 13/13 : ENTRYPOINT ["/src/checkoutservice"]
 ---> Running in 2d02ecc3cb11
Removing intermediate container 2d02ecc3cb11
 ---> 08cf51d99fdf
Successfully built 08cf51d99fdf
Successfully tagged mwanthi/checkoutservice:latest
[Pipeline] sh
+ docker tag mwanthi/checkoutservice mwanthi/checkoutservice:v0.0.2
[Pipeline] sh
+ docker push mwanthi/checkoutservice:v0.0.2
The push refers to repository [docker.io/mwanthi/checkoutservice]
6be17df6008d: Preparing
a89c7d69df60: Preparing
a89c7d69df60: Pushed
6be17df6008d: Pushed
v0.0.2: digest: sha256:c13b841540cfc9219ecb3d8def55ffdcd2d4fc7339ff506fc76d853c38ada0dc size: 735
[Pipeline] sh
+ docker push mwanthi/checkoutservice:latest
The push refers to repository [docker.io/mwanthi/checkoutservice]
6be17df6008d: Preparing
a89c7d69df60: Preparing
a89c7d69df60: Layer already exists
6be17df6008d: Layer already exists
latest: digest: sha256:c13b841540cfc9219ecb3d8def55ffdcd2d4fc7339ff506fc76d853c38ada0dc size: 735
[Pipeline] sh
+ sed -i  -e s|mwanthi/checkoutservice:v0.0.1|mwanthi/checkoutservice:v0.0.2|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/checkoutservice/checkoutservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/checkoutservice:latest
Untagged: mwanthi/checkoutservice:latest
[Pipeline] sh
+ docker rmi mwanthi/checkoutservice:v0.0.2
Untagged: mwanthi/checkoutservice:v0.0.2
Untagged: mwanthi/checkoutservice@sha256:c13b841540cfc9219ecb3d8def55ffdcd2d4fc7339ff506fc76d853c38ada0dc
Deleted: sha256:08cf51d99fdffda261ae5ba385e32fe86c6cee436d624f1ecd3d1bfa3ca70ec3
Deleted: sha256:b43b095f2999fd582a2bf55593d1ef21a58618e925be551d52c591975f05680c
Deleted: sha256:82dfdf1cda86bbaaadcdd89835c053fb2ee45cc6afbb404b54f0d9b85d5c90fd
Deleted: sha256:938e14b393e94a5dd83c6a57ea14e1616bb43991596da1fb96e394c0b65d27bc
Deleted: sha256:fa012573996fad494093d670c45a3e899a8e310266e1462eb5d5d0bc4f816df4
Deleted: sha256:a0a70f67895f8f634c23efa2f7ab6b82ea24b4ede914bd081b65dbdcec6879e0
Deleted: sha256:a89c7d69df60412666a9c54d5f9f1f8e469de636bf177bd52e95d8185b67be2c
[Pipeline] sh
+ docker image prune -f
Deleted Images:
untagged: eclipse-temurin@sha256:e538e34d1df871c9b7da571582cdc49538f1eaee1dacbfb317a3e7f54abeebae
deleted: sha256:8f2c4d2db18138a62c2909325b9a54cb6a56885677b63dc4112e6ddf5f7d5068
deleted: sha256:99ba35ce4ccdf3054328068fca527e01f982022080d511b8eb511e83691d14fb
deleted: sha256:9dc2cb186df39106837f9fa0e34e3ac2a79f236884786b129855012eba6a087e
deleted: sha256:9da6d3fa050f2af139a8a18f1b2a79aa074edea5b48c4cccee4c705c36a70a20
deleted: sha256:b377a06bb335a8a8479b6250210414cc8c616cffbf307de3c0c4c6aa5c2d7d9e
deleted: sha256:b15b682e901dd27efdf436ce837a94c729c0b78c44431d5b5ca3ccca1bed40da
deleted: sha256:b3338a44dcdafd94cb4659cbf0e8c75328c65e008ab5a95f779c4d6f0c5593ed
deleted: sha256:f9fc2711f702ceffca91e3b0e56fbca03bcaace799290553b4d7c5d5233a3c5a
deleted: sha256:8a3745cdef846263ecc930fa4ad26493d452e2aad8d928c06abf6136cba56b0e
deleted: sha256:85258fe45a49eb4012050e0275504ca8fdec533764c6073c16490add6d34f42f
deleted: sha256:f5f6781566ae813cfded41e35e1280ca2358ff53ff5c058f1023b2fbb8364aff
deleted: sha256:001cb48c5c4718f2ce6c3e4679084f0c8fdde79dde4e68d5395844f9edc3a757
deleted: sha256:11cb2108175f1cf294da6a13114b210aa5750cb36c0f746198d96e02a8d72660
deleted: sha256:dee93d512d28d4561601e7d5dd7482df57e865158ab463266eb20ac742bfa8c1
deleted: sha256:c533a19f7ab72f6b882bc593bb64340cec98bbf99e7249b7eae18ce382a3059c
deleted: sha256:304074a59a97e86597d666f086eb5db1d37db75a1d0f64684714566ff34a0a68
deleted: sha256:d8cd0b590eb6f23c47fc6f73c45d8f2477a06c6a8c2d5c5e06610342fb5745da

Total reclaimed space: 1.192GB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Rebuilding and Pushing shippingservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/e165e0a1-b479-4d6d-aacb-7a642ed4f27b/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ + grepawk image: mwanthi/shippingservice:[^[:space:]]* {gsub(/^v/, ""); print} /home/ubuntu/workspace/microservices-build/kubernetes-manifests/shippingservice/shippingservice.yaml

+ awk -F : {print $3}
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app/src/shippingservice
[Pipeline] {
[Pipeline] sh
+ docker build --no-cache -t mwanthi/shippingservice .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  181.2kB

Step 1/14 : FROM golang:1.23.1-alpine@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06 AS builder
 ---> b5ada884192f
Step 2/14 : WORKDIR /src
 ---> Running in 9eb48c2befc4
Removing intermediate container 9eb48c2befc4
 ---> 078cefc8c228
Step 3/14 : COPY go.mod go.sum ./
 ---> 333686fd79c4
Step 4/14 : RUN go mod download
 ---> Running in 6e8f1ac5a72d
Removing intermediate container 6e8f1ac5a72d
 ---> 248c853bd868
Step 5/14 : COPY . .
 ---> 0b8d8abf30e8
Step 6/14 : ARG SKAFFOLD_GO_GCFLAGS
 ---> Running in 33a1037b2712
Removing intermediate container 33a1037b2712
 ---> b608fcc4931c
Step 7/14 : RUN CGO_ENABLED=0 GOOS=linux go build -gcflags="${SKAFFOLD_GO_GCFLAGS}" -o /go/bin/shippingservice .
 ---> Running in af55e4ffb7c3
Removing intermediate container af55e4ffb7c3
 ---> 4796aeaa9c14
Step 8/14 : FROM scratch
 ---> 
Step 9/14 : WORKDIR /src
 ---> Running in d2267e728f32
Removing intermediate container d2267e728f32
 ---> 711cc0b4fd15
Step 10/14 : COPY --from=builder /go/bin/shippingservice /src/shippingservice
 ---> f76356bc426a
Step 11/14 : ENV APP_PORT=50051
 ---> Running in 179bfaffa1de
Removing intermediate container 179bfaffa1de
 ---> 85b79146adce
Step 12/14 : ENV GOTRACEBACK=single
 ---> Running in ce4a5673313c
Removing intermediate container ce4a5673313c
 ---> 36d41f649a64
Step 13/14 : EXPOSE 50051
 ---> Running in d20103ea1907
Removing intermediate container d20103ea1907
 ---> f5c634a400b1
Step 14/14 : ENTRYPOINT ["/src/shippingservice"]
 ---> Running in 8c0e9b4fbf37
Removing intermediate container 8c0e9b4fbf37
 ---> abcc2556c23d
Successfully built abcc2556c23d
Successfully tagged mwanthi/shippingservice:latest
[Pipeline] sh
+ docker tag mwanthi/shippingservice mwanthi/shippingservice:v0.0.2
[Pipeline] sh
+ docker push mwanthi/shippingservice:v0.0.2
The push refers to repository [docker.io/mwanthi/shippingservice]
f175807ea7e2: Preparing
741d43162a6c: Preparing
741d43162a6c: Pushed
f175807ea7e2: Pushed
v0.0.2: digest: sha256:5e4a3f852fbb746a88b05add7f3cc176b1bad8df8f45847af4ff365e2627d9ba size: 735
[Pipeline] sh
+ docker push mwanthi/shippingservice:latest
The push refers to repository [docker.io/mwanthi/shippingservice]
f175807ea7e2: Preparing
741d43162a6c: Preparing
741d43162a6c: Layer already exists
f175807ea7e2: Layer already exists
latest: digest: sha256:5e4a3f852fbb746a88b05add7f3cc176b1bad8df8f45847af4ff365e2627d9ba size: 735
[Pipeline] sh
+ sed -i  -e s|mwanthi/shippingservice:v0.0.1|mwanthi/shippingservice:v0.0.2|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/shippingservice/shippingservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/shippingservice:latest
Untagged: mwanthi/shippingservice:latest
[Pipeline] sh
+ docker rmi mwanthi/shippingservice:v0.0.2
Untagged: mwanthi/shippingservice:v0.0.2
Untagged: mwanthi/shippingservice@sha256:5e4a3f852fbb746a88b05add7f3cc176b1bad8df8f45847af4ff365e2627d9ba
Deleted: sha256:abcc2556c23d558bd868ba4483154e0129a4eeb19b76230389112c7a7228af71
Deleted: sha256:f5c634a400b14d5a48daff7ba44f2c1d5c1a6c8f7435eb53b9b8120b49df1d62
Deleted: sha256:36d41f649a64422ea87ed3da6e94544be7bfbdce92dd3b8474e8ec19a88e87e7
Deleted: sha256:85b79146adce644a919deb03254a6c2a441dfd32c11da4925109cbc3c6483c58
Deleted: sha256:f76356bc426a985829462d5ab6480a7e14cde2e766cbf5dbcef7ef5e865f6127
Deleted: sha256:04d7ca923ecb8fd14a15f47721fc1691ecb0e92bfe5a2102a75e27f6f2b79205
Deleted: sha256:711cc0b4fd15b7f4328283092f5780916f7c50af2a34b8f96fd2bba7939adbbd
Deleted: sha256:741d43162a6cea2983659609434a9deb4a8f6801f8eb71dfe1bb69c1d2caee80
[Pipeline] sh
+ docker image prune -f
Deleted Images:
deleted: sha256:4796aeaa9c14457b8ec6dcbae821883899ef4e2a570d70b40baabceac9e895d0
deleted: sha256:1dd6435ff6e1574d44c5a4c5a49682b12a14c9e2928bd62ad424a3adc10b8386
deleted: sha256:b608fcc4931c9f062e79e956629644261fb1a9e5e4865fea538ead0d20a4edd3
deleted: sha256:0b8d8abf30e81132e6a58cea47a979c004b195c50569ef9db103bbba1de5392e
deleted: sha256:a48007f41f7d6d5a15f549cb6ab6b56330f25ebfaf270c4e99b3712b019be507
deleted: sha256:248c853bd868cd15555008993b4a01e8cad98f1388a0b32ed034848b9942887f
deleted: sha256:30404b6b2e77efcb93df001790b70c43a7faed2829b01589941f7ccb342db8ae
deleted: sha256:333686fd79c4e7b790114784e5e81b74ff1564c3aab82d83ced93ce2a8de449b
deleted: sha256:3476bb50d42843c1b496374ec4f40f273a665a05c8b07f0e0154cb05dd465d0f
deleted: sha256:078cefc8c2289c18a1b92e5da64ae4b7de398064e866ec1107d5c637e24dc140
deleted: sha256:d82549e60ae0a931162830ac0989475b2d5ec2480a54d8d005d741762137b9c7

Total reclaimed space: 724.1MB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Push K8S Manifest changes to Github)
[Pipeline] script
[Pipeline] {
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/kubernetes-manifests
[Pipeline] {
[Pipeline] sh
+ git config --local user.name D-Mwanth
+ git config --local user.email dmwanthi2@gmail.com
[Pipeline] sh
+ git add .
[Pipeline] sh
+ git commit -m Updated Deployment Manifest-Build 2
[main 4107081] Updated Deployment Manifest-Build 2
 3 files changed, 3 insertions(+), 3 deletions(-)
[Pipeline] withCredentials
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
Masking supported pattern matches of $GIT_PASSWORD or $GIT_ASKPASS
[Pipeline] {
[Pipeline] sh
+ git push https://github.com/D-Mwanth/kubernetes-manifests.git main
To https://github.com/D-Mwanth/kubernetes-manifests.git
   073329f..4107081  main -> main
[Pipeline] }
[Pipeline] // withCredentials
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Declarative: Post Actions)
[Pipeline] echo
Sending Slack Notification...
[Pipeline] script
[Pipeline] {
[Pipeline] slackSend
Slack Send Pipeline step running, values are - baseUrl: <empty>, teamDomain: bughunter-space, channel: #jenkins-bot, color: #11a611, botUser: false, tokenCredentialId: slack-access-key, notifyCommitters: false, iconEmoji: <empty>, username: <empty>, timestamp: <empty>
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] End of Pipeline
Finished: SUCCESS