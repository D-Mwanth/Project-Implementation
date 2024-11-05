Started by user master
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
Cloning the remote Git repository
Cloning with configured refspecs honoured and without tags
Cloning repository https://github.com/D-Mwanth/microservices-build-pipeline
 > git init /var/lib/jenkins/workspace/microservices-build@libs/234dc070aeabf2f6fd2cc25edb7cf070e38fbb9da90f665b14113b67e5d42a5b # timeout=10
Fetching upstream changes from https://github.com/D-Mwanth/microservices-build-pipeline
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
 > git fetch --no-tags --force --progress -- https://github.com/D-Mwanth/microservices-build-pipeline +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git config remote.origin.url https://github.com/D-Mwanth/microservices-build-pipeline # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
Avoid second fetch
Checking out Revision 41dbfceafe950081224dafe54589ec1f35aee9e3 (main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 41dbfceafe950081224dafe54589ec1f35aee9e3 # timeout=10
Commit message: "Updated `buildOrReBuildImage.groovy` to remove dangling images"
First time build. Skipping changelog.
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
Cloning repository https://github.com/D-Mwanth/microservices-build-pipeline
 > git init /home/ubuntu/workspace/microservices-build # timeout=10
Fetching upstream changes from https://github.com/D-Mwanth/microservices-build-pipeline
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
 > git fetch --tags --force --progress -- https://github.com/D-Mwanth/microservices-build-pipeline +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git config remote.origin.url https://github.com/D-Mwanth/microservices-build-pipeline # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
Avoid second fetch
Checking out Revision 41dbfceafe950081224dafe54589ec1f35aee9e3 (refs/remotes/origin/main)
 > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 41dbfceafe950081224dafe54589ec1f35aee9e3 # timeout=10
Commit message: "Updated `buildOrReBuildImage.groovy` to remove dangling images"
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] withEnv
[Pipeline] {
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
Cloning repository https://github.com/D-Mwanth/microservices-app.git
 > git init /home/ubuntu/workspace/microservices-build/microservices-app # timeout=10
Fetching upstream changes from https://github.com/D-Mwanth/microservices-app.git
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
 > git fetch --tags --force --progress -- https://github.com/D-Mwanth/microservices-app.git +refs/heads/*:refs/remotes/origin/* # timeout=10
Avoid second fetch
Checking out Revision a136e140a2ce54a1dfbe8182fb996785d77ff6cf (refs/remotes/origin/main)
Commit message: "initial commit"
First time build. Skipping changelog.
[Pipeline] }
[Pipeline] // dir
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/kubernetes-manifests
[Pipeline] {
[Pipeline] git
The recommended git tool is: NONE
No credentials specified
Cloning the remote Git repository
 > git config remote.origin.url https://github.com/D-Mwanth/microservices-app.git # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
 > git config core.sparsecheckout # timeout=10
 > git checkout -f a136e140a2ce54a1dfbe8182fb996785d77ff6cf # timeout=10
 > git branch -a -v --no-abbrev # timeout=10
 > git checkout -b main a136e140a2ce54a1dfbe8182fb996785d77ff6cf # timeout=10
Avoid second fetch
Checking out Revision 65bcf89214e72b5f294bc4c98685c600d92691b0 (refs/remotes/origin/main)
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
 > git checkout -f 65bcf89214e72b5f294bc4c98685c600d92691b0 # timeout=10
 > git branch -a -v --no-abbrev # timeout=10
 > git checkout -b main 65bcf89214e72b5f294bc4c98685c600d92691b0 # timeout=10
Commit message: "Initial k8s manifests commit"
First time build. Skipping changelog.
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
+ cut -d / -f 2
+ git ls-tree --name-only -r HEAD
+ uniq
+ grep -v /.gitignore
+ sort
+ grep ^src/
+ tr \n  
[Pipeline] }
[Pipeline] // dir
[Pipeline] echo
Services to Build: [adservice, cartservice, checkoutservice, currencyservice, emailservice, frontend, loadgenerator, paymentservice, productcatalogservice, recommendationservice, shippingservice]
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
[adservice, cartservice, checkoutservice, currencyservice, emailservice, frontend, loadgenerator, paymentservice, productcatalogservice, recommendationservice, shippingservice]
[Pipeline] echo
Tracking and building adservice service...
[Pipeline] sh
+ echo adservice
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Building and Pushing adservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/9bb239cd-fcb7-4dcd-b981-441146ffe557/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ grep image: mwanthi/adservice:[^[:space:]]* /home/ubuntu/workspace/microservices-build/kubernetes-manifests/adservice/adservice.yaml
+ awk -F : {print $3}
+ awk {gsub(/^v/, ""); print}
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
fe18bb7e114f: Verifying Checksum
fe18bb7e114f: Download complete
32b824d45c61: Verifying Checksum
32b824d45c61: Download complete
7c7bdd063feb: Verifying Checksum
7c7bdd063feb: Download complete
28f1e2918031: Verifying Checksum
28f1e2918031: Download complete
581ebfe08d3f: Verifying Checksum
581ebfe08d3f: Download complete
32b824d45c61: Pull complete
fe18bb7e114f: Pull complete
581ebfe08d3f: Pull complete
7c7bdd063feb: Pull complete
28f1e2918031: Pull complete
Digest: sha256:e538e34d1df871c9b7da571582cdc49538f1eaee1dacbfb317a3e7f54abeebae
Status: Downloaded newer image for eclipse-temurin:21@sha256:e538e34d1df871c9b7da571582cdc49538f1eaee1dacbfb317a3e7f54abeebae
 ---> 8f2c4d2db181
Step 2/14 : WORKDIR /app
 ---> Running in 0aee79728090
Removing intermediate container 0aee79728090
 ---> 8e0aeaf9b893
Step 3/14 : COPY ["build.gradle", "gradlew", "./"]
 ---> 0272f4911683
Step 4/14 : COPY gradle gradle
 ---> 3c634577fcac
Step 5/14 : RUN chmod +x gradlew
 ---> Running in 9e39ee3bc3c0
Removing intermediate container 9e39ee3bc3c0
 ---> 4b0815724bf3
Step 6/14 : RUN ./gradlew downloadRepos
 ---> Running in ebbd59cddafb
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
Removing intermediate container ebbd59cddafb
 ---> e3c0dbd02999
Step 7/14 : COPY . .
 ---> b365f6bae59b
Step 8/14 : RUN chmod +x gradlew
 ---> Running in d49cfcf86bbd
Removing intermediate container d49cfcf86bbd
 ---> c079822921aa
Step 9/14 : RUN ./gradlew installDist
 ---> Running in 9c7429c3aee9
Starting a Gradle Daemon, 1 incompatible and 1 stopped Daemons could not be reused, use --status for details
> Task :extractIncludeProto
> Task :extractProto
> Task :generateProto

> Task :compileJava
[91mNote: /app/src/main/java/hipstershop/AdService.java uses or overrides a deprecated API.
[0m[91mNote: Recompile with -Xlint:deprecation for details.
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

BUILD SUCCESSFUL in 37s
9 actionable tasks: 9 executed
Removing intermediate container 9c7429c3aee9
 ---> c85ca68a40ad
Step 10/14 : FROM eclipse-temurin:21.0.4_7-jre-alpine@sha256:8cc1202a100e72f6e91bf05ab274b373a5def789ab6d9e3e293a61236662ac27
docker.io/library/eclipse-temurin:21.0.4_7-jre-alpine@sha256:8cc1202a100e72f6e91bf05ab274b373a5def789ab6d9e3e293a61236662ac27: Pulling from library/eclipse-temurin
43c4264eed91: Pulling fs layer
4fb0eeeb44ea: Pulling fs layer
6be5feca48e3: Pulling fs layer
0efe887b0486: Pulling fs layer
c4d7b64b67a4: Pulling fs layer
0efe887b0486: Waiting
c4d7b64b67a4: Waiting
43c4264eed91: Verifying Checksum
43c4264eed91: Download complete
4fb0eeeb44ea: Verifying Checksum
4fb0eeeb44ea: Download complete
43c4264eed91: Pull complete
0efe887b0486: Verifying Checksum
0efe887b0486: Download complete
c4d7b64b67a4: Verifying Checksum
c4d7b64b67a4: Download complete
6be5feca48e3: Verifying Checksum
6be5feca48e3: Download complete
4fb0eeeb44ea: Pull complete
6be5feca48e3: Pull complete
0efe887b0486: Pull complete
c4d7b64b67a4: Pull complete
Digest: sha256:8cc1202a100e72f6e91bf05ab274b373a5def789ab6d9e3e293a61236662ac27
Status: Downloaded newer image for eclipse-temurin:21.0.4_7-jre-alpine@sha256:8cc1202a100e72f6e91bf05ab274b373a5def789ab6d9e3e293a61236662ac27
 ---> 29ce5002d122
Step 11/14 : WORKDIR /app
 ---> Running in e653ac367209
Removing intermediate container e653ac367209
 ---> 664626ac1f52
Step 12/14 : COPY --from=builder /app .
 ---> 32a56b030b96
Step 13/14 : EXPOSE 9555
 ---> Running in ebcd07be5d71
Removing intermediate container ebcd07be5d71
 ---> d3df7253c58c
Step 14/14 : ENTRYPOINT ["/app/build/install/hipstershop/bin/AdService"]
 ---> Running in c031e4d854bc
Removing intermediate container c031e4d854bc
 ---> 127b40cf9f09
Successfully built 127b40cf9f09
Successfully tagged mwanthi/adservice:latest
[Pipeline] sh
+ docker tag mwanthi/adservice mwanthi/adservice:v0.0.1
[Pipeline] sh
+ docker push mwanthi/adservice:v0.0.1
The push refers to repository [docker.io/mwanthi/adservice]
382c799f0277: Preparing
da000c619bac: Preparing
71e8cc6fa9c8: Preparing
44a76360121e: Preparing
13407d63b650: Preparing
01d3f5d5a6c9: Preparing
63ca1fbb43ae: Preparing
63ca1fbb43ae: Waiting
01d3f5d5a6c9: Waiting
44a76360121e: Mounted from library/eclipse-temurin
71e8cc6fa9c8: Mounted from library/eclipse-temurin
13407d63b650: Mounted from library/eclipse-temurin
01d3f5d5a6c9: Mounted from library/eclipse-temurin
da000c619bac: Pushed
63ca1fbb43ae: Mounted from library/eclipse-temurin
382c799f0277: Pushed
v0.0.1: digest: sha256:958a2bc8906d958fd59ceac77443045696bf8784dcf9c2734b4ca7e9260a8f2f size: 1784
[Pipeline] sh
+ docker push mwanthi/adservice:latest
The push refers to repository [docker.io/mwanthi/adservice]
382c799f0277: Preparing
da000c619bac: Preparing
71e8cc6fa9c8: Preparing
44a76360121e: Preparing
13407d63b650: Preparing
01d3f5d5a6c9: Preparing
63ca1fbb43ae: Preparing
01d3f5d5a6c9: Waiting
63ca1fbb43ae: Waiting
382c799f0277: Layer already exists
44a76360121e: Layer already exists
da000c619bac: Layer already exists
13407d63b650: Layer already exists
71e8cc6fa9c8: Layer already exists
01d3f5d5a6c9: Layer already exists
63ca1fbb43ae: Layer already exists
latest: digest: sha256:958a2bc8906d958fd59ceac77443045696bf8784dcf9c2734b4ca7e9260a8f2f size: 1784
[Pipeline] sh
+ sed -i  -e s|mwanthi/adservice:v0.0.1|mwanthi/adservice:v0.0.1|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/adservice/adservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/adservice:latest
Untagged: mwanthi/adservice:latest
[Pipeline] sh
+ docker rmi mwanthi/adservice:v0.0.1
Untagged: mwanthi/adservice:v0.0.1
Untagged: mwanthi/adservice@sha256:958a2bc8906d958fd59ceac77443045696bf8784dcf9c2734b4ca7e9260a8f2f
Deleted: sha256:127b40cf9f097a9b4e1c2d5f9c717f7ca81084971f47050eb1ac0afd915f40b3
Deleted: sha256:d3df7253c58ca265825cdef44244ae52d13a8514025e438beb497189cc1749be
Deleted: sha256:32a56b030b965fe06cbde85ba7bfb55eef4190a277854687ee63d360c19d51be
Deleted: sha256:ae3c1442dea01ba1d77fc65f2a3f8d1fe0a2983e2707b06f6f1d6795680a55be
Deleted: sha256:664626ac1f522ac20fb9f375383c0a76f1bfce3be30ba3eabeae7540c8b2f8c5
Deleted: sha256:4d6790626899760723b8fcb7e9638390eb237928ef1bf9628267a167b5db236c
[Pipeline] sh
+ docker image prune -f
Deleted Images:
deleted: sha256:c85ca68a40ad1a889c267d74a7326fba6c5e6757e2f1bfd19001dc0f429a6d74
deleted: sha256:e0657f05257f9ce214b894433d3eee08ab32c632d649b10cb144522d31358112
deleted: sha256:c079822921aab0262aa489f9fe7d1ffd47928d2d077705bde4d9520e3adaafdb
deleted: sha256:e48b1eb4a6a94bbe1a440a50309e4ef24d1d973868e2199bff65a66ea528ff8f
deleted: sha256:b365f6bae59b138038857a4ba00c209a244a3bb9634f60111e6b259f15ba1c32
deleted: sha256:f4cbcc0c13b84ad65a1d16ef8592c0b2df1eda91070079579944a2e7e51170f1
deleted: sha256:e3c0dbd029994635f8b18bbed093eb815a5a975f9ede159075a0ebc984a20d6b
deleted: sha256:8f5e325073d948b5fcfc1b6cc570f65bf219520114627f3272ca3a29ebc665fb
deleted: sha256:4b0815724bf3a7bb17b13099f24426f54eddcf3477aa8ddd1325ed1fab9d9678
deleted: sha256:de17a1e2d8aeaf2f0eccc95a6b5666d24810b31730a0aeb46aa82f4130c119d2
deleted: sha256:3c634577fcac8963dd88c3385832d213c48ab5c3e5d5e0cb44d666d2277c88bf
deleted: sha256:ee55322d857acb46d41c5a1693c688e1993f521cf8a28bdbf094bf4fac75276b
deleted: sha256:0272f491168384eee18c2da7aecbdd68922ff8bee3ae57e31b8534741ed20681
deleted: sha256:1834cf6382be05295aaadcb51c0e3db3019018669f6164db24fa384e753971e7
deleted: sha256:8e0aeaf9b89351b20698d54e3956779ceb49e4b483913eff1bd6e80bd2ca47ea
deleted: sha256:89b907c326403a5ef43f6582fb49d6d8192674cf2ace63634c745308059eaee1
untagged: eclipse-temurin@sha256:8cc1202a100e72f6e91bf05ab274b373a5def789ab6d9e3e293a61236662ac27
deleted: sha256:29ce5002d122a67eb0e9e1889f04519886ef38baea0a9410138798e8d95ff6af
deleted: sha256:ce97291ed233db35a28773072a090d19c498336b3b3d2cc8b368957d9641bb6e
deleted: sha256:9da47462cb0d9f03cbf3a2ed03b764e239c6ea4a078aad49e8e005c75d083a86
deleted: sha256:f3752a5777d03e8e36ca44c11e15482b3c7433a2ca77ee0ef289348a9b4f9ab7
deleted: sha256:7dada8fb0e360803bb185862b64e2c6c0888266672bd22c268a713bd6fbd57ea
deleted: sha256:63ca1fbb43ae5034640e5e6cb3e083e05c290072c5366fcaa9d62435a4cced85

Total reclaimed space: 435MB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] echo
Tracking and building cartservice service...
[Pipeline] sh
+ echo cartservice
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Building and Pushing cartservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/a9c2c097-cb76-4991-8a45-370d6e828a64/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ grep image: mwanthi/cartservice:[^[:space:]]* /home/ubuntu/workspace/microservices-build/kubernetes-manifests/cartservice/cartservice.yaml
+ awk -F : {print $3}
+ awk {gsub(/^v/, ""); print}
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app/src/cartservice/src
[Pipeline] {
[Pipeline] sh
+ docker build --no-cache -t mwanthi/cartservice .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  41.98kB

Step 1/13 : FROM mcr.microsoft.com/dotnet/sdk:8.0.402-noble@sha256:96bd4e90b80d82f8e77512ec0893d7ae18b4d2af332b9e68ed575c9842cc175c AS builder
mcr.microsoft.com/dotnet/sdk:8.0.402-noble@sha256:96bd4e90b80d82f8e77512ec0893d7ae18b4d2af332b9e68ed575c9842cc175c: Pulling from dotnet/sdk
eda6120e237e: Pulling fs layer
2dd566c6fb25: Pulling fs layer
6f9ebdc85d10: Pulling fs layer
938e58acdc32: Pulling fs layer
fa7d889fdfed: Pulling fs layer
eebe9ae8127e: Pulling fs layer
d109bf5d5e0e: Pulling fs layer
c5c05fabc85a: Pulling fs layer
f1ea2f24eaf9: Pulling fs layer
eebe9ae8127e: Waiting
938e58acdc32: Waiting
fa7d889fdfed: Waiting
d109bf5d5e0e: Waiting
c5c05fabc85a: Waiting
f1ea2f24eaf9: Waiting
6f9ebdc85d10: Verifying Checksum
6f9ebdc85d10: Download complete
eda6120e237e: Verifying Checksum
eda6120e237e: Download complete
2dd566c6fb25: Verifying Checksum
2dd566c6fb25: Download complete
938e58acdc32: Verifying Checksum
938e58acdc32: Download complete
fa7d889fdfed: Verifying Checksum
fa7d889fdfed: Download complete
eebe9ae8127e: Verifying Checksum
eebe9ae8127e: Download complete
d109bf5d5e0e: Verifying Checksum
d109bf5d5e0e: Download complete
f1ea2f24eaf9: Verifying Checksum
f1ea2f24eaf9: Download complete
eda6120e237e: Pull complete
2dd566c6fb25: Pull complete
6f9ebdc85d10: Pull complete
c5c05fabc85a: Verifying Checksum
c5c05fabc85a: Download complete
938e58acdc32: Pull complete
fa7d889fdfed: Pull complete
eebe9ae8127e: Pull complete
d109bf5d5e0e: Pull complete
c5c05fabc85a: Pull complete
f1ea2f24eaf9: Pull complete
Digest: sha256:96bd4e90b80d82f8e77512ec0893d7ae18b4d2af332b9e68ed575c9842cc175c
Status: Downloaded newer image for mcr.microsoft.com/dotnet/sdk:8.0.402-noble@sha256:96bd4e90b80d82f8e77512ec0893d7ae18b4d2af332b9e68ed575c9842cc175c
 ---> dd4de239ba90
Step 2/13 : WORKDIR /app
 ---> Running in 272bdf050583
Removing intermediate container 272bdf050583
 ---> 06bb7079f623
Step 3/13 : COPY cartservice.csproj .
 ---> 15eb0cc8af88
Step 4/13 : RUN dotnet restore cartservice.csproj     -r linux-x64
 ---> Running in bae466b19e26
  Determining projects to restore...
  Restored /app/cartservice.csproj (in 10.96 sec).
Removing intermediate container bae466b19e26
 ---> 74b50b478639
Step 5/13 : COPY . .
 ---> cf91fcecdd4b
Step 6/13 : RUN dotnet publish cartservice.csproj     -p:PublishSingleFile=true     -r linux-x64     --self-contained true     -p:PublishTrimmed=true     -p:TrimMode=full     -c release     -o /cartservice
 ---> Running in f3bae4494e79
  Determining projects to restore...
  Restored /app/cartservice.csproj (in 1.25 sec).
  cartservice -> /app/bin/release/net8.0/linux-x64/cartservice.dll
  Optimizing assemblies for size. This process might take a while.
ILLink : Trim analysis warning IL2026: System.Data.DataSet.System.Xml.Serialization.IXmlSerializable.GetSchema(): Using member 'System.Data.DataSet.WriteXmlSchema(DataSet, XmlWriter)' which has 'RequiresUnreferencedCodeAttribute' can break functionality when trimming application code. DataSet.GetSchema uses TypeDescriptor and XmlSerialization underneath which are not trimming safe. Members from serialized types may be trimmed if not referenced directly. [/app/cartservice.csproj]
ILLink : Trim analysis warning IL2026: System.Data.DataSet.System.Xml.Serialization.IXmlSerializable.ReadXml(XmlReader): Using member 'System.Data.DataSet.ReadXmlSerializableInternal(XmlReader)' which has 'RequiresUnreferencedCodeAttribute' can break functionality when trimming application code. DataSet.ReadXml uses XmlSerialization underneath which is not trimming safe. Members from serialized types may be trimmed if not referenced directly. [/app/cartservice.csproj]
ILLink : Trim analysis warning IL2026: System.Data.DataSet.System.Xml.Serialization.IXmlSerializable.WriteXml(XmlWriter): Using member 'System.Data.DataSet.WriteXmlInternal(XmlWriter)' which has 'RequiresUnreferencedCodeAttribute' can break functionality when trimming application code. DataSet.WriteXml uses XmlSerialization underneath which is not trimming safe. Members from serialized types may be trimmed if not referenced directly. [/app/cartservice.csproj]
ILLink : Trim analysis warning IL2026: System.Data.DataTable.System.Xml.Serialization.IXmlSerializable.GetSchema(): Using member 'System.Data.DataTable.GetXmlSchema()' which has 'RequiresUnreferencedCodeAttribute' can break functionality when trimming application code. DataTable.GetSchema uses TypeDescriptor and XmlSerialization underneath which are not trimming safe. Members from serialized types may be trimmed if not referenced directly. [/app/cartservice.csproj]
ILLink : Trim analysis warning IL2026: System.Data.DataTable.System.Xml.Serialization.IXmlSerializable.ReadXml(XmlReader): Using member 'System.Data.DataTable.ReadXmlSerializableInternal(XmlReader)' which has 'RequiresUnreferencedCodeAttribute' can break functionality when trimming application code. DataTable.ReadXml uses XmlSerialization underneath which is not trimming safe. Members from serialized types may be trimmed if not referenced directly. [/app/cartservice.csproj]
ILLink : Trim analysis warning IL2026: System.Data.DataTable.System.Xml.Serialization.IXmlSerializable.WriteXml(XmlWriter): Using member 'System.Data.DataTable.WriteXmlInternal(XmlWriter)' which has 'RequiresUnreferencedCodeAttribute' can break functionality when trimming application code. DataTable.WriteXml uses XmlSerialization underneath which is not trimming safe. Members from serialized types may be trimmed if not referenced directly. [/app/cartservice.csproj]
/root/.nuget/packages/google.api.gax.grpc/4.8.0/lib/netstandard2.0/Google.Api.Gax.Grpc.dll : warning IL2104: Assembly 'Google.Api.Gax.Grpc' produced trim warnings. For more information see https://aka.ms/dotnet-illink/libraries [/app/cartservice.csproj]
/root/.nuget/packages/google.apis.core/1.67.0/lib/net6.0/Google.Apis.Core.dll : warning IL2104: Assembly 'Google.Apis.Core' produced trim warnings. For more information see https://aka.ms/dotnet-illink/libraries [/app/cartservice.csproj]
/root/.nuget/packages/google.cloud.spanner.data/4.6.0/lib/netstandard2.1/Google.Cloud.Spanner.Data.dll : warning IL2104: Assembly 'Google.Cloud.Spanner.Data' produced trim warnings. For more information see https://aka.ms/dotnet-illink/libraries [/app/cartservice.csproj]
/root/.nuget/packages/newtonsoft.json/13.0.3/lib/net6.0/Newtonsoft.Json.dll : warning IL2104: Assembly 'Newtonsoft.Json' produced trim warnings. For more information see https://aka.ms/dotnet-illink/libraries [/app/cartservice.csproj]
  cartservice -> /cartservice/
Removing intermediate container f3bae4494e79
 ---> 32282737e1a4
Step 7/13 : FROM mcr.microsoft.com/dotnet/runtime-deps:8.0.8-noble-chiseled@sha256:7c86350773464d70bd15b2804c0e52f6c0f6b27d05d0fc607ff16abeb84dedd0
mcr.microsoft.com/dotnet/runtime-deps:8.0.8-noble-chiseled@sha256:7c86350773464d70bd15b2804c0e52f6c0f6b27d05d0fc607ff16abeb84dedd0: Pulling from dotnet/runtime-deps
cf7438e86b3e: Pulling fs layer
4f4fb700ef54: Pulling fs layer
4f4fb700ef54: Verifying Checksum
4f4fb700ef54: Download complete
cf7438e86b3e: Verifying Checksum
cf7438e86b3e: Download complete
cf7438e86b3e: Pull complete
4f4fb700ef54: Pull complete
Digest: sha256:7c86350773464d70bd15b2804c0e52f6c0f6b27d05d0fc607ff16abeb84dedd0
Status: Downloaded newer image for mcr.microsoft.com/dotnet/runtime-deps:8.0.8-noble-chiseled@sha256:7c86350773464d70bd15b2804c0e52f6c0f6b27d05d0fc607ff16abeb84dedd0
 ---> 0caa444b9553
Step 8/13 : WORKDIR /app
 ---> Running in 14746ccd122b
Removing intermediate container 14746ccd122b
 ---> 65680c4014fc
Step 9/13 : COPY --from=builder /cartservice .
 ---> 9490851d62e3
Step 10/13 : EXPOSE 7070
 ---> Running in c354a4a738fc
Removing intermediate container c354a4a738fc
 ---> 2bebfc633d2e
Step 11/13 : ENV DOTNET_EnableDiagnostics=0     ASPNETCORE_HTTP_PORTS=7070
 ---> Running in 3f25d8197525
Removing intermediate container 3f25d8197525
 ---> f69caa58831f
Step 12/13 : USER 1000
 ---> Running in fca59fc06184
Removing intermediate container fca59fc06184
 ---> 41440340c055
Step 13/13 : ENTRYPOINT ["/app/cartservice"]
 ---> Running in be94026620a9
Removing intermediate container be94026620a9
 ---> 992b35674dc8
Successfully built 992b35674dc8
Successfully tagged mwanthi/cartservice:latest
[Pipeline] sh
+ docker tag mwanthi/cartservice mwanthi/cartservice:v0.0.1
[Pipeline] sh
+ docker push mwanthi/cartservice:v0.0.1
The push refers to repository [docker.io/mwanthi/cartservice]
18c2204db888: Preparing
e3bd413403c3: Preparing
5f70bf18a086: Preparing
aced8747a5df: Preparing
5f70bf18a086: Pushed
e3bd413403c3: Pushed
aced8747a5df: Pushed
18c2204db888: Pushed
v0.0.1: digest: sha256:698cd3d9d34ed310d9a7a866fbcccf3d0cd7f5937e4cfa7c4bf4f9de9ab1bd24 size: 1152
[Pipeline] sh
+ docker push mwanthi/cartservice:latest
The push refers to repository [docker.io/mwanthi/cartservice]
18c2204db888: Preparing
e3bd413403c3: Preparing
5f70bf18a086: Preparing
aced8747a5df: Preparing
e3bd413403c3: Layer already exists
5f70bf18a086: Layer already exists
18c2204db888: Layer already exists
aced8747a5df: Layer already exists
latest: digest: sha256:698cd3d9d34ed310d9a7a866fbcccf3d0cd7f5937e4cfa7c4bf4f9de9ab1bd24 size: 1152
[Pipeline] sh
+ sed -i  -e s|mwanthi/cartservice:v0.0.1|mwanthi/cartservice:v0.0.1|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/cartservice/cartservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/cartservice:latest
Untagged: mwanthi/cartservice:latest
[Pipeline] sh
+ docker rmi mwanthi/cartservice:v0.0.1
Untagged: mwanthi/cartservice:v0.0.1
Untagged: mwanthi/cartservice@sha256:698cd3d9d34ed310d9a7a866fbcccf3d0cd7f5937e4cfa7c4bf4f9de9ab1bd24
Deleted: sha256:992b35674dc88f44179a0eeb00e7d751ba6c05d7e0eb4f82b7bb5ed1a75ef64b
Deleted: sha256:41440340c055e10d0ad7d3253d3f8116faf1a2ed363b83ea661997b37f295c31
Deleted: sha256:f69caa58831f42c14de0ace61816412cb9a292b93d08cd91619efbc43620b5d5
Deleted: sha256:2bebfc633d2ed53ae9b391734f6d56253aecdb0776e3fb2674ec3c0cc722ae73
Deleted: sha256:9490851d62e3b1a85aa0446559b67d5ac8985d12fb73c2026de66f13697cc3a3
Deleted: sha256:6d830ad014d4d32f71134e8451bf0731f52d55048eea9cc23213e6a876c005b9
Deleted: sha256:65680c4014fc566302061efc254f41cd07702dbee5897e2f4fef67c6837b0d40
Deleted: sha256:1e6e5f86405649290d83c36398eaa8636c8e8094b71f43fccc3d55878f9f0cf6
[Pipeline] sh
+ docker image prune -f
Deleted Images:
deleted: sha256:32282737e1a49d6647dc41a8a6bb839f16051278397f61542673168dfa17d8c2
deleted: sha256:d6cb7538e72c803b9e0a82396b8741cbd977b8fa4763a4a952fd1358bdb653fa
deleted: sha256:cf91fcecdd4b4f928e4086ff7caad00a2478ce4a52a2e3c73730b413cbdc3937
deleted: sha256:9e356614d04b24cd708d061c9ac891f6c26100c1b4e240384277707b4c0d79b8
deleted: sha256:74b50b4786390139a6665bcd4b44599cb0405359990b0be15ce3f783d02152b9
deleted: sha256:691761f562fe54bfc8e0d82f499f0e7d3d8325140329d262237009576a953d97
deleted: sha256:15eb0cc8af88ac2c313a230cfc9ac1b658f6d7b433d791402c998d64ac256b8c
deleted: sha256:4e63bc4bd3ddd2d87013f80401d4b9b7abd74296849be22fa343323a54a63318
deleted: sha256:06bb7079f623fc9fdf35d3a82a4de5dd38ed1721ea4a6063cb615014ae0800fc
deleted: sha256:1050d3e76c700a3c5895f92f0ce23069493945287f4d651c37c271875b4ebaef
untagged: mcr.microsoft.com/dotnet/runtime-deps@sha256:7c86350773464d70bd15b2804c0e52f6c0f6b27d05d0fc607ff16abeb84dedd0
deleted: sha256:0caa444b9553f6437f34bfaf2735222daaa8e8229c6ffd8d5790d4668187a7b3
deleted: sha256:e3a5029126a8a2fe975d40bcbd16aaf0f470e59e0d354e4d7efc62d9b8d43cde
deleted: sha256:aced8747a5df72ac43e8622598aeb74199b8a66b19a2b809053c85507eca30dd
untagged: eclipse-temurin@sha256:e538e34d1df871c9b7da571582cdc49538f1eaee1dacbfb317a3e7f54abeebae
deleted: sha256:8f2c4d2db18138a62c2909325b9a54cb6a56885677b63dc4112e6ddf5f7d5068
deleted: sha256:99ba35ce4ccdf3054328068fca527e01f982022080d511b8eb511e83691d14fb
deleted: sha256:9dc2cb186df39106837f9fa0e34e3ac2a79f236884786b129855012eba6a087e
deleted: sha256:9da6d3fa050f2af139a8a18f1b2a79aa074edea5b48c4cccee4c705c36a70a20
deleted: sha256:b377a06bb335a8a8479b6250210414cc8c616cffbf307de3c0c4c6aa5c2d7d9e
deleted: sha256:b15b682e901dd27efdf436ce837a94c729c0b78c44431d5b5ca3ccca1bed40da

Total reclaimed space: 1.076GB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] echo
Tracking and building checkoutservice service...
[Pipeline] sh
+ echo checkoutservice
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Building and Pushing checkoutservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/b06f1168-b099-4167-ba2a-c8cd12ab9846/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ + grep image: mwanthi/checkoutservice:[^[:space:]]* /home/ubuntu/workspace/microservices-build/kubernetes-manifests/checkoutservice/checkoutservice.yaml
awk {gsub(/^v/, ""); print}
+ awk -F : {print $3}
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
4f4fb700ef54: Verifying Checksum
4f4fb700ef54: Download complete
ab19dfae90ef: Pull complete
e7bff916ab0c: Verifying Checksum
e7bff916ab0c: Download complete
e7bff916ab0c: Pull complete
78cee99375e3: Pull complete
4f4fb700ef54: Pull complete
Digest: sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06
Status: Downloaded newer image for golang:1.23.1-alpine@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06
 ---> b5ada884192f
Step 2/13 : WORKDIR /src
 ---> Running in 1d2d651c2add
Removing intermediate container 1d2d651c2add
 ---> c0f33ec9050a
Step 3/13 : COPY go.mod go.sum ./
 ---> ece129880f83
Step 4/13 : RUN go mod download
 ---> Running in 39ecbbf10ac9
Removing intermediate container 39ecbbf10ac9
 ---> deb4a89321a5
Step 5/13 : COPY . .
 ---> 42963e27b699
Step 6/13 : ARG SKAFFOLD_GO_GCFLAGS
 ---> Running in c3a7683d3fd0
Removing intermediate container c3a7683d3fd0
 ---> 67a29b87765b
Step 7/13 : RUN CGO_ENABLED=0 GOOS=linux go build -gcflags="${SKAFFOLD_GO_GCFLAGS}" -o /checkoutservice .
 ---> Running in 63fdc8d32c10
Removing intermediate container 63fdc8d32c10
 ---> cc6dd170dea4
Step 8/13 : FROM scratch
 ---> 
Step 9/13 : WORKDIR /src
 ---> Running in a2d2f12ae2ed
Removing intermediate container a2d2f12ae2ed
 ---> 8a032780f325
Step 10/13 : COPY --from=builder /checkoutservice /src/checkoutservice
 ---> 7c26b1e290ff
Step 11/13 : ENV GOTRACEBACK=single
 ---> Running in 77fb67f91c6a
Removing intermediate container 77fb67f91c6a
 ---> ffd1a37f4982
Step 12/13 : EXPOSE 5050
 ---> Running in 727a33e2057f
Removing intermediate container 727a33e2057f
 ---> 764a64501164
Step 13/13 : ENTRYPOINT ["/src/checkoutservice"]
 ---> Running in 94060a8d6f86
Removing intermediate container 94060a8d6f86
 ---> 10f282ad523c
Successfully built 10f282ad523c
Successfully tagged mwanthi/checkoutservice:latest
[Pipeline] sh
+ docker tag mwanthi/checkoutservice mwanthi/checkoutservice:v0.0.1
[Pipeline] sh
+ docker push mwanthi/checkoutservice:v0.0.1
The push refers to repository [docker.io/mwanthi/checkoutservice]
cdda7718740b: Preparing
9ac104d5a691: Preparing
9ac104d5a691: Pushed
cdda7718740b: Pushed
v0.0.1: digest: sha256:73f714386bee8da625db850b53a0f84fb3028a29bf951a437905f42ad27fad47 size: 735
[Pipeline] sh
+ docker push mwanthi/checkoutservice:latest
The push refers to repository [docker.io/mwanthi/checkoutservice]
cdda7718740b: Preparing
9ac104d5a691: Preparing
9ac104d5a691: Layer already exists
cdda7718740b: Layer already exists
latest: digest: sha256:73f714386bee8da625db850b53a0f84fb3028a29bf951a437905f42ad27fad47 size: 735
[Pipeline] sh
+ sed -i  -e s|mwanthi/checkoutservice:v0.0.1|mwanthi/checkoutservice:v0.0.1|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/checkoutservice/checkoutservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/checkoutservice:latest
Untagged: mwanthi/checkoutservice:latest
[Pipeline] sh
+ docker rmi mwanthi/checkoutservice:v0.0.1
Untagged: mwanthi/checkoutservice:v0.0.1
Untagged: mwanthi/checkoutservice@sha256:73f714386bee8da625db850b53a0f84fb3028a29bf951a437905f42ad27fad47
Deleted: sha256:10f282ad523cb5e96c3df835ddd2b4002a8a7e4f5cf9dff1056586c49e6bfd84
Deleted: sha256:764a64501164d3fa49c8e3d587283e5e4581a4a2f915eae169f4fd180ed8a276
Deleted: sha256:ffd1a37f4982a64d2565663bb561ac1384a46d8c8228457b90d3fbd5b58f5f15
Deleted: sha256:7c26b1e290ff5390867c3555d7492666ef145efe03d30f324ee75e6294cf9b3b
Deleted: sha256:0cd147ef548ebf4ed023260219c599ceed1e78089d40f4bf34743e110a7db102
Deleted: sha256:8a032780f325d54ab8804c61560a511a29d9529e0c05e922e90621361c331722
Deleted: sha256:9ac104d5a691fc34087b289ab2d857d1594990ec68845bcd560aadb7db59df03
[Pipeline] sh
+ docker image prune -f
Deleted Images:
untagged: mcr.microsoft.com/dotnet/sdk@sha256:96bd4e90b80d82f8e77512ec0893d7ae18b4d2af332b9e68ed575c9842cc175c
deleted: sha256:dd4de239ba9094fb0a7bc52618fd3c9021ed121fad6287cbcb9aafa47f59b96b
deleted: sha256:d3fc9dfc64cf86609e421ad97e1f5c6a3674443f390fb41190bfbe0e1842e934
deleted: sha256:7fcade5a481dfc0f331a0b73840562ea8db59976a0137a10ae8d86815de8884c
deleted: sha256:027b54af7f816e9ba112886eec3dbebe576c377d93f21e7420419305c470fe5a
deleted: sha256:045a089241ec7b17d9d20aaf3bafb1499a384f22476c6bb16aefdf7ce49a5b74
deleted: sha256:cb91441af5f9cea41f71985324fedfc8e6bf1b073e56789a5351f9cf2ee613e3
deleted: sha256:1e5dc62cc473b67f3507fb6ca6a940d682617dac1ec293085aa2fb7002282954
deleted: sha256:f64e6f4a9b89c0b51d80ed80743f5502403111e277f2c94191b111e3cebf9286
deleted: sha256:35084d43d6561edfa2c1a57e36f0f6bf26263824ca5f73ae0d34be80a4f51ded
deleted: sha256:ba8dbc5b24b59c2e6aff3639f32c5402af5e30be686342d08925ad852bd8c7c4
deleted: sha256:cc6dd170dea487e74b955a917b7d37b4994b5d199d87d30e698cd664054a5d52
deleted: sha256:6c406276037d10350963a61d349cfcdb14b0c774c30ec3e45237371ef0a1336a
deleted: sha256:67a29b87765b32ac450af79514b3f7299f994b010d745124f3f486d3eeb65590
deleted: sha256:42963e27b6993da9987d3f712c305600821f9db5b45265ca266307e9cefc0333
deleted: sha256:eebd906048b0d3675c892ebee8cef6ae3034a32e4d5bf4c0a69d4f0fc67843b5
deleted: sha256:deb4a89321a55c5e3e3cebc3bfb916c236e8f60d14d73ef0e0414c3baef46478
deleted: sha256:d0957059271bd7976c6ebd1a319b96744d47983153e5cb323fb25a8837c40c98
deleted: sha256:ece129880f831aee505519012cf2d9783c5625d64e8cc40e2a61dadfc807d3b1
deleted: sha256:4bbd64099f2fbe2b362bf00b47082864e61f41535ecf0764435a40c97465f931
deleted: sha256:c0f33ec9050af457457035ebe22cce2ae89d5ff820f76c40286ce937c36da618
deleted: sha256:486ffef9ca59344bb94e9ac0c34a63c3f26bb5aa0ee8fbb39b14221b040d2541

Total reclaimed space: 1.562GB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] echo
Tracking and building currencyservice service...
[Pipeline] sh
+ echo currencyservice
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Building and Pushing currencyservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/802309be-8b77-4a14-bc65-384bef61390c/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ + awkgrep {gsub(/^v/, ""); print} image: mwanthi/currencyservice:[^[:space:]]*
 /home/ubuntu/workspace/microservices-build/kubernetes-manifests/currencyservice/currencyservice.yaml
+ awk -F : {print $3}
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app/src/currencyservice
[Pipeline] {
[Pipeline] sh
+ docker build --no-cache -t mwanthi/currencyservice .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  149.5kB

Step 1/12 : FROM node:20.17.0-alpine@sha256:2d07db07a2df6830718ae2a47db6fedce6745f5bcd174c398f2acdda90a11c03 AS builder
docker.io/library/node:20.17.0-alpine@sha256:2d07db07a2df6830718ae2a47db6fedce6745f5bcd174c398f2acdda90a11c03: Pulling from library/node
43c4264eed91: Already exists
c36270121b0c: Pulling fs layer
842cd80f9366: Pulling fs layer
737da86e5e86: Pulling fs layer
737da86e5e86: Verifying Checksum
737da86e5e86: Download complete
842cd80f9366: Verifying Checksum
842cd80f9366: Download complete
c36270121b0c: Verifying Checksum
c36270121b0c: Download complete
c36270121b0c: Pull complete
842cd80f9366: Pull complete
737da86e5e86: Pull complete
Digest: sha256:2d07db07a2df6830718ae2a47db6fedce6745f5bcd174c398f2acdda90a11c03
Status: Downloaded newer image for node:20.17.0-alpine@sha256:2d07db07a2df6830718ae2a47db6fedce6745f5bcd174c398f2acdda90a11c03
 ---> 45a59611ca84
Step 2/12 : RUN apk add --update --no-cache     python3     make     g++
 ---> Running in 90b57aca5c5d
fetch https://dl-cdn.alpinelinux.org/alpine/v3.20/main/x86_64/APKINDEX.tar.gz
fetch https://dl-cdn.alpinelinux.org/alpine/v3.20/community/x86_64/APKINDEX.tar.gz
(1/29) Installing libstdc++-dev (13.2.1_git20240309-r0)
(2/29) Installing jansson (2.14-r4)
(3/29) Installing zstd-libs (1.5.6-r0)
(4/29) Installing binutils (2.42-r0)
(5/29) Installing libgomp (13.2.1_git20240309-r0)
(6/29) Installing libatomic (13.2.1_git20240309-r0)
(7/29) Installing gmp (6.3.0-r1)
(8/29) Installing isl26 (0.26-r1)
(9/29) Installing mpfr4 (4.2.1-r0)
(10/29) Installing mpc1 (1.3.1-r1)
(11/29) Installing gcc (13.2.1_git20240309-r0)
(12/29) Installing musl-dev (1.2.5-r0)
(13/29) Installing g++ (13.2.1_git20240309-r0)
(14/29) Installing make (4.4.1-r2)
(15/29) Installing libbz2 (1.0.8-r6)
(16/29) Installing libexpat (2.6.3-r0)
(17/29) Installing libffi (3.4.6-r0)
(18/29) Installing gdbm (1.23-r1)
(19/29) Installing xz-libs (5.6.2-r0)
(20/29) Installing mpdecimal (4.0.0-r0)
(21/29) Installing ncurses-terminfo-base (6.4_p20240420-r1)
(22/29) Installing libncursesw (6.4_p20240420-r1)
(23/29) Installing libpanelw (6.4_p20240420-r1)
(24/29) Installing readline (8.2.10-r0)
(25/29) Installing sqlite-libs (3.45.3-r1)
(26/29) Installing python3 (3.12.7-r0)
(27/29) Installing python3-pycache-pyc0 (3.12.7-r0)
(28/29) Installing pyc (3.12.7-r0)
(29/29) Installing python3-pyc (3.12.7-r0)
Executing busybox-1.36.1-r29.trigger
OK: 255 MiB in 45 packages
Removing intermediate container 90b57aca5c5d
 ---> fc44337a7c8c
Step 3/12 : WORKDIR /usr/src/app
 ---> Running in 21cacb416d9c
Removing intermediate container 21cacb416d9c
 ---> 13bd181433bb
Step 4/12 : COPY package*.json ./
 ---> ce9cf5615d29
Step 5/12 : RUN npm install --only=production
 ---> Running in 944884d7ce9b
[91mnpm warn config only Use `--omit=dev` to omit dev dependencies from the install.
[0m[91mnpm warn deprecated @opentelemetry/exporter-otlp-grpc@0.26.0: Please use trace and metric specific exporters @opentelemetry/exporter-trace-otlp-grpc and @opentelemetry/exporter-metrics-otlp-grpc
[0m[91mnpm warn deprecated @opentelemetry/exporter-otlp-http@0.26.0: Please use trace and metric specific exporters @opentelemetry/exporter-trace-otlp-http and @opentelemetry/exporter-metrics-otlp-http
[0m[91mnpm warn deprecated @opentelemetry/api-metrics@0.26.0: Please use @opentelemetry/api >= 1.3.0
[0m[91mnpm warn deprecated @opentelemetry/sdk-metrics-base@0.26.0: Please use @opentelemetry/sdk-metrics
[0m
added 278 packages, and audited 279 packages in 18s

20 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
[91mnpm notice
npm notice New minor version of npm available! 10.8.2 -> 10.9.0
npm notice Changelog: https://github.com/npm/cli/releases/tag/v10.9.0
npm notice To update run: npm install -g npm@10.9.0
npm notice
[0mRemoving intermediate container 944884d7ce9b
 ---> 614185fc3b3c
Step 6/12 : FROM alpine:3.20.3@sha256:beefdbd8a1da6d2915566fde36db9db0b524eb737fc57cd1367effd16dc0d06d
docker.io/library/alpine:3.20.3@sha256:beefdbd8a1da6d2915566fde36db9db0b524eb737fc57cd1367effd16dc0d06d: Pulling from library/alpine
43c4264eed91: Already exists
Digest: sha256:beefdbd8a1da6d2915566fde36db9db0b524eb737fc57cd1367effd16dc0d06d
Status: Downloaded newer image for alpine:3.20.3@sha256:beefdbd8a1da6d2915566fde36db9db0b524eb737fc57cd1367effd16dc0d06d
 ---> 91ef0af61f39
Step 7/12 : RUN apk add --no-cache nodejs
 ---> Running in 13940f40e5e0
fetch https://dl-cdn.alpinelinux.org/alpine/v3.20/main/x86_64/APKINDEX.tar.gz
fetch https://dl-cdn.alpinelinux.org/alpine/v3.20/community/x86_64/APKINDEX.tar.gz
(1/11) Installing ca-certificates (20240705-r0)
(2/11) Installing libgcc (13.2.1_git20240309-r0)
(3/11) Installing libstdc++ (13.2.1_git20240309-r0)
(4/11) Installing ada-libs (2.7.8-r0)
(5/11) Installing libbase64 (0.5.2-r0)
(6/11) Installing brotli-libs (1.1.0-r2)
(7/11) Installing c-ares (1.33.1-r0)
(8/11) Installing icu-data-en (74.2-r0)
Executing icu-data-en-74.2-r0.post-install
[91m*
* If you need ICU with non-English locales and legacy charset support, install
* package icu-data-full.
*
[0m(9/11) Installing icu-libs (74.2-r0)
(10/11) Installing nghttp2-libs (1.62.1-r0)
(11/11) Installing nodejs (20.15.1-r0)
Executing busybox-1.36.1-r29.trigger
Executing ca-certificates-20240705-r0.trigger
OK: 61 MiB in 25 packages
Removing intermediate container 13940f40e5e0
 ---> 2a2e7550356a
Step 8/12 : WORKDIR /usr/src/app
 ---> Running in af5df97c2322
Removing intermediate container af5df97c2322
 ---> 12a707a8f071
Step 9/12 : COPY --from=builder /usr/src/app/node_modules ./node_modules
 ---> 4bafbb5d98cd
Step 10/12 : COPY . .
 ---> 44bcc92e6d7f
Step 11/12 : EXPOSE 7000
 ---> Running in 100887ddc329
Removing intermediate container 100887ddc329
 ---> e1894aca8f70
Step 12/12 : ENTRYPOINT [ "node", "server.js" ]
 ---> Running in 1c994b0f54a4
Removing intermediate container 1c994b0f54a4
 ---> d60eef61334e
Successfully built d60eef61334e
Successfully tagged mwanthi/currencyservice:latest
[Pipeline] sh
+ docker tag mwanthi/currencyservice mwanthi/currencyservice:v0.0.1
[Pipeline] sh
+ docker push mwanthi/currencyservice:v0.0.1
The push refers to repository [docker.io/mwanthi/currencyservice]
d49b9cfce787: Preparing
2bbae9672adc: Preparing
8fd989bad3dd: Preparing
5808611ae72b: Preparing
63ca1fbb43ae: Preparing
63ca1fbb43ae: Mounted from mwanthi/adservice
8fd989bad3dd: Pushed
d49b9cfce787: Pushed
5808611ae72b: Pushed
2bbae9672adc: Pushed
v0.0.1: digest: sha256:da4dc30c113ff27ac9b7b924a60e2aa553a9391f0a1b7145498e7bc7992b62db size: 1368
[Pipeline] sh
+ docker push mwanthi/currencyservice:latest
The push refers to repository [docker.io/mwanthi/currencyservice]
d49b9cfce787: Preparing
2bbae9672adc: Preparing
8fd989bad3dd: Preparing
5808611ae72b: Preparing
63ca1fbb43ae: Preparing
2bbae9672adc: Layer already exists
63ca1fbb43ae: Layer already exists
5808611ae72b: Layer already exists
8fd989bad3dd: Layer already exists
d49b9cfce787: Layer already exists
latest: digest: sha256:da4dc30c113ff27ac9b7b924a60e2aa553a9391f0a1b7145498e7bc7992b62db size: 1368
[Pipeline] sh
+ sed -i  -e s|mwanthi/currencyservice:v0.0.1|mwanthi/currencyservice:v0.0.1|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/currencyservice/currencyservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/currencyservice:latest
Untagged: mwanthi/currencyservice:latest
[Pipeline] sh
+ docker rmi mwanthi/currencyservice:v0.0.1
Untagged: mwanthi/currencyservice:v0.0.1
Untagged: mwanthi/currencyservice@sha256:da4dc30c113ff27ac9b7b924a60e2aa553a9391f0a1b7145498e7bc7992b62db
Deleted: sha256:d60eef61334ef87aa8a225b5f5f570839ea1921af868900825e872fb48956de5
Deleted: sha256:e1894aca8f704462ab2ab5d52f1d33e9b525644dc34f1e9a5e09ce7dbed50681
Deleted: sha256:44bcc92e6d7f2cac6268394960a5ad4b923a75593abe6ac9f70f0c54f8adc7d3
Deleted: sha256:4429cbad38a59b24bdbab0fe12c1566da5b583d85ea49701d421cac6b95a6567
Deleted: sha256:4bafbb5d98cdd4b09352aceb8e9f83c8920d1721f43d5e0d7fd6ba066044027d
Deleted: sha256:4d24c8854a5d7aea286f3b7aa5322407ad647f3f4202aef4dedd5e2ea5336ac0
Deleted: sha256:12a707a8f071871dc28b2ba6101e1f13ca0bc1664b51c374b0dbd2e83f95b2d1
Deleted: sha256:a7b4ab0db323f08ada6559e6cb15d6916f525abaf837b069d484612e810ee817
Deleted: sha256:2a2e7550356ad6a98db7c98529154d7671c524098f2281dc4230604863f4acbc
Deleted: sha256:e19efad4eba284d79fdde8a44dce7658d487899d9b3b58a7dbaf86d7cf100bfb
[Pipeline] sh
+ docker image prune -f
Deleted Images:
untagged: alpine@sha256:beefdbd8a1da6d2915566fde36db9db0b524eb737fc57cd1367effd16dc0d06d
deleted: sha256:91ef0af61f39ece4d6710e465df5ed6ca12112358344fd51ae6a3b886634148b
deleted: sha256:614185fc3b3c02505e34c2af0f672f3a407b88d89c62e6de58b387a0452cb988
deleted: sha256:2b3463a9cae753d26cef3098dd018c73cb46d89a67089188af777633fbeedbf6
deleted: sha256:ce9cf5615d29ce8db4a5e941bbf38f4f0c758d96acf5f3e7be9dafa7cc14c9ef
deleted: sha256:c8e4a7961e89c4aac7dc0fa34db36c17b16015c9d7e8db469d23c62ebf290808
deleted: sha256:13bd181433bb608801d974e443c9668e2576e643edc3c13247e7d0af2707c84c
deleted: sha256:1a0dabd8d60633e85f58a9a14e5b62fde9081ce4e464409f38f6bb12a968085c
deleted: sha256:fc44337a7c8c57697466061290e9d1542cbb580fde2436c33e7aa76416f8a7d5
deleted: sha256:aae9e902019da8445e960671846ba38ea3f2c583cabd4a4ae8b38e0ebd9d01de
untagged: golang@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06
deleted: sha256:b5ada884192f173018fcb39688bd70545669ab105941231067ea5dbed4ac6914
deleted: sha256:2968ff6a64392cda70b3e2cb5d6e62723bfdc18fe68b46382c971bee002890a2
deleted: sha256:768a08d8d838830bce342fdf82d2051ad375b9a575cb6cb685f8841bc16f5ae2
deleted: sha256:7c37ab7540e48469f2843766943fb1f5b838efe35a1e500268f45f1b6ba88942
deleted: sha256:db287705205f639bdfff0f98a53c5b40608826ee5ab2b1180bcf22eec319953c

Total reclaimed space: 642.8MB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] echo
Tracking and building emailservice service...
[Pipeline] sh
+ echo emailservice
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Building and Pushing emailservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/56b515fe-4cd2-4ff5-bc04-0744f9e020ec/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ + grep image: mwanthi/emailservice:[^[:space:]]* /home/ubuntu/workspace/microservices-build/kubernetes-manifests/emailservice/emailservice.yaml
awk {gsub(/^v/, ""); print}
+ awk -F : {print $3}
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app/src/emailservice
[Pipeline] {
[Pipeline] sh
+ docker build --no-cache -t mwanthi/emailservice .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  67.07kB

Step 1/13 : FROM python:3.12.6-slim@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26 AS base
docker.io/library/python:3.12.6-slim@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26: Pulling from library/python
302e3ee49805: Pulling fs layer
699edf835b1b: Pulling fs layer
417a872b7725: Pulling fs layer
9795987f6d21: Pulling fs layer
9795987f6d21: Waiting
699edf835b1b: Verifying Checksum
699edf835b1b: Download complete
417a872b7725: Verifying Checksum
417a872b7725: Download complete
302e3ee49805: Verifying Checksum
302e3ee49805: Download complete
9795987f6d21: Verifying Checksum
9795987f6d21: Download complete
302e3ee49805: Pull complete
699edf835b1b: Pull complete
417a872b7725: Pull complete
9795987f6d21: Pull complete
Digest: sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26
Status: Downloaded newer image for python:3.12.6-slim@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26
 ---> 86b8b6de4ba2
Step 2/13 : FROM base AS builder
 ---> 86b8b6de4ba2
Step 3/13 : RUN apt-get -qq update     && apt-get install -y --no-install-recommends         wget g++     && rm -rf /var/lib/apt/lists/*
 ---> Running in fa1a1a50b3b0
Reading package lists...
Building dependency tree...
Reading state information...
The following additional packages will be installed:
  binutils binutils-common binutils-x86-64-linux-gnu cpp cpp-12 g++-12 gcc
  gcc-12 libasan8 libatomic1 libbinutils libc-dev-bin libc6-dev libcc1-0
  libcrypt-dev libctf-nobfd0 libctf0 libgcc-12-dev libgomp1 libgprofng0
  libisl23 libitm1 libjansson4 liblsan0 libmpc3 libmpfr6 libnsl-dev libpsl5
  libquadmath0 libstdc++-12-dev libtirpc-dev libtsan2 libubsan1 linux-libc-dev
  rpcsvc-proto
Suggested packages:
  binutils-doc cpp-doc gcc-12-locales cpp-12-doc g++-multilib g++-12-multilib
  gcc-12-doc gcc-multilib make manpages-dev autoconf automake libtool flex
  bison gdb gcc-doc gcc-12-multilib glibc-doc libstdc++-12-doc
Recommended packages:
  manpages manpages-dev libc-devtools publicsuffix
The following NEW packages will be installed:
  binutils binutils-common binutils-x86-64-linux-gnu cpp cpp-12 g++ g++-12 gcc
  gcc-12 libasan8 libatomic1 libbinutils libc-dev-bin libc6-dev libcc1-0
  libcrypt-dev libctf-nobfd0 libctf0 libgcc-12-dev libgomp1 libgprofng0
  libisl23 libitm1 libjansson4 liblsan0 libmpc3 libmpfr6 libnsl-dev libpsl5
  libquadmath0 libstdc++-12-dev libtirpc-dev libtsan2 libubsan1 linux-libc-dev
  rpcsvc-proto wget
0 upgraded, 37 newly installed, 0 to remove and 0 not upgraded.
Need to get 64.2 MB of archives.
After this operation, 262 MB of additional disk space will be used.
Get:1 http://deb.debian.org/debian bookworm/main amd64 libpsl5 amd64 0.21.2-1 [58.7 kB]
Get:2 http://deb.debian.org/debian bookworm/main amd64 wget amd64 1.21.3-1+b2 [984 kB]
Get:3 http://deb.debian.org/debian bookworm/main amd64 binutils-common amd64 2.40-2 [2487 kB]
Get:4 http://deb.debian.org/debian bookworm/main amd64 libbinutils amd64 2.40-2 [572 kB]
Get:5 http://deb.debian.org/debian bookworm/main amd64 libctf-nobfd0 amd64 2.40-2 [153 kB]
Get:6 http://deb.debian.org/debian bookworm/main amd64 libctf0 amd64 2.40-2 [89.8 kB]
Get:7 http://deb.debian.org/debian bookworm/main amd64 libgprofng0 amd64 2.40-2 [812 kB]
Get:8 http://deb.debian.org/debian bookworm/main amd64 libjansson4 amd64 2.14-2 [40.8 kB]
Get:9 http://deb.debian.org/debian bookworm/main amd64 binutils-x86-64-linux-gnu amd64 2.40-2 [2246 kB]
Get:10 http://deb.debian.org/debian bookworm/main amd64 binutils amd64 2.40-2 [65.0 kB]
Get:11 http://deb.debian.org/debian bookworm/main amd64 libisl23 amd64 0.25-1.1 [683 kB]
Get:12 http://deb.debian.org/debian bookworm/main amd64 libmpfr6 amd64 4.2.0-1 [701 kB]
Get:13 http://deb.debian.org/debian bookworm/main amd64 libmpc3 amd64 1.3.1-1 [51.5 kB]
Get:14 http://deb.debian.org/debian bookworm/main amd64 cpp-12 amd64 12.2.0-14 [9764 kB]
Get:15 http://deb.debian.org/debian bookworm/main amd64 cpp amd64 4:12.2.0-3 [6836 B]
Get:16 http://deb.debian.org/debian bookworm/main amd64 libcc1-0 amd64 12.2.0-14 [41.7 kB]
Get:17 http://deb.debian.org/debian bookworm/main amd64 libgomp1 amd64 12.2.0-14 [116 kB]
Get:18 http://deb.debian.org/debian bookworm/main amd64 libitm1 amd64 12.2.0-14 [26.1 kB]
Get:19 http://deb.debian.org/debian bookworm/main amd64 libatomic1 amd64 12.2.0-14 [9328 B]
Get:20 http://deb.debian.org/debian bookworm/main amd64 libasan8 amd64 12.2.0-14 [2195 kB]
Get:21 http://deb.debian.org/debian bookworm/main amd64 liblsan0 amd64 12.2.0-14 [969 kB]
Get:22 http://deb.debian.org/debian bookworm/main amd64 libtsan2 amd64 12.2.0-14 [2196 kB]
Get:23 http://deb.debian.org/debian bookworm/main amd64 libubsan1 amd64 12.2.0-14 [883 kB]
Get:24 http://deb.debian.org/debian bookworm/main amd64 libquadmath0 amd64 12.2.0-14 [144 kB]
Get:25 http://deb.debian.org/debian bookworm/main amd64 libgcc-12-dev amd64 12.2.0-14 [2437 kB]
Get:26 http://deb.debian.org/debian bookworm/main amd64 gcc-12 amd64 12.2.0-14 [19.3 MB]
Get:27 http://deb.debian.org/debian bookworm/main amd64 gcc amd64 4:12.2.0-3 [5216 B]
Get:28 http://deb.debian.org/debian bookworm/main amd64 libc-dev-bin amd64 2.36-9+deb12u8 [46.3 kB]
Get:29 http://deb.debian.org/debian-security bookworm-security/main amd64 linux-libc-dev amd64 6.1.112-1 [2043 kB]
Get:30 http://deb.debian.org/debian bookworm/main amd64 libcrypt-dev amd64 1:4.4.33-2 [118 kB]
Get:31 http://deb.debian.org/debian bookworm/main amd64 libtirpc-dev amd64 1.3.3+ds-1 [191 kB]
Get:32 http://deb.debian.org/debian bookworm/main amd64 libnsl-dev amd64 1.3.0-2 [66.4 kB]
Get:33 http://deb.debian.org/debian bookworm/main amd64 rpcsvc-proto amd64 1.4.3-1 [63.3 kB]
Get:34 http://deb.debian.org/debian bookworm/main amd64 libc6-dev amd64 2.36-9+deb12u8 [1900 kB]
Get:35 http://deb.debian.org/debian bookworm/main amd64 libstdc++-12-dev amd64 12.2.0-14 [2046 kB]
Get:36 http://deb.debian.org/debian bookworm/main amd64 g++-12 amd64 12.2.0-14 [10.7 MB]
Get:37 http://deb.debian.org/debian bookworm/main amd64 g++ amd64 4:12.2.0-3 [1356 B]
[91mdebconf: delaying package configuration, since apt-utils is not installed
[0mFetched 64.2 MB in 1s (85.2 MB/s)
Selecting previously unselected package libpsl5:amd64.
(Reading database ... 
(Reading database ... 5%
(Reading database ... 10%
(Reading database ... 15%
(Reading database ... 20%
(Reading database ... 25%
(Reading database ... 30%
(Reading database ... 35%
(Reading database ... 40%
(Reading database ... 45%
(Reading database ... 50%
(Reading database ... 55%
(Reading database ... 60%
(Reading database ... 65%
(Reading database ... 70%
(Reading database ... 75%
(Reading database ... 80%
(Reading database ... 85%
(Reading database ... 90%
(Reading database ... 95%
(Reading database ... 100%
(Reading database ... 6695 files and directories currently installed.)
Preparing to unpack .../00-libpsl5_0.21.2-1_amd64.deb ...
Unpacking libpsl5:amd64 (0.21.2-1) ...
Selecting previously unselected package wget.
Preparing to unpack .../01-wget_1.21.3-1+b2_amd64.deb ...
Unpacking wget (1.21.3-1+b2) ...
Selecting previously unselected package binutils-common:amd64.
Preparing to unpack .../02-binutils-common_2.40-2_amd64.deb ...
Unpacking binutils-common:amd64 (2.40-2) ...
Selecting previously unselected package libbinutils:amd64.
Preparing to unpack .../03-libbinutils_2.40-2_amd64.deb ...
Unpacking libbinutils:amd64 (2.40-2) ...
Selecting previously unselected package libctf-nobfd0:amd64.
Preparing to unpack .../04-libctf-nobfd0_2.40-2_amd64.deb ...
Unpacking libctf-nobfd0:amd64 (2.40-2) ...
Selecting previously unselected package libctf0:amd64.
Preparing to unpack .../05-libctf0_2.40-2_amd64.deb ...
Unpacking libctf0:amd64 (2.40-2) ...
Selecting previously unselected package libgprofng0:amd64.
Preparing to unpack .../06-libgprofng0_2.40-2_amd64.deb ...
Unpacking libgprofng0:amd64 (2.40-2) ...
Selecting previously unselected package libjansson4:amd64.
Preparing to unpack .../07-libjansson4_2.14-2_amd64.deb ...
Unpacking libjansson4:amd64 (2.14-2) ...
Selecting previously unselected package binutils-x86-64-linux-gnu.
Preparing to unpack .../08-binutils-x86-64-linux-gnu_2.40-2_amd64.deb ...
Unpacking binutils-x86-64-linux-gnu (2.40-2) ...
Selecting previously unselected package binutils.
Preparing to unpack .../09-binutils_2.40-2_amd64.deb ...
Unpacking binutils (2.40-2) ...
Selecting previously unselected package libisl23:amd64.
Preparing to unpack .../10-libisl23_0.25-1.1_amd64.deb ...
Unpacking libisl23:amd64 (0.25-1.1) ...
Selecting previously unselected package libmpfr6:amd64.
Preparing to unpack .../11-libmpfr6_4.2.0-1_amd64.deb ...
Unpacking libmpfr6:amd64 (4.2.0-1) ...
Selecting previously unselected package libmpc3:amd64.
Preparing to unpack .../12-libmpc3_1.3.1-1_amd64.deb ...
Unpacking libmpc3:amd64 (1.3.1-1) ...
Selecting previously unselected package cpp-12.
Preparing to unpack .../13-cpp-12_12.2.0-14_amd64.deb ...
Unpacking cpp-12 (12.2.0-14) ...
Selecting previously unselected package cpp.
Preparing to unpack .../14-cpp_4%3a12.2.0-3_amd64.deb ...
Unpacking cpp (4:12.2.0-3) ...
Selecting previously unselected package libcc1-0:amd64.
Preparing to unpack .../15-libcc1-0_12.2.0-14_amd64.deb ...
Unpacking libcc1-0:amd64 (12.2.0-14) ...
Selecting previously unselected package libgomp1:amd64.
Preparing to unpack .../16-libgomp1_12.2.0-14_amd64.deb ...
Unpacking libgomp1:amd64 (12.2.0-14) ...
Selecting previously unselected package libitm1:amd64.
Preparing to unpack .../17-libitm1_12.2.0-14_amd64.deb ...
Unpacking libitm1:amd64 (12.2.0-14) ...
Selecting previously unselected package libatomic1:amd64.
Preparing to unpack .../18-libatomic1_12.2.0-14_amd64.deb ...
Unpacking libatomic1:amd64 (12.2.0-14) ...
Selecting previously unselected package libasan8:amd64.
Preparing to unpack .../19-libasan8_12.2.0-14_amd64.deb ...
Unpacking libasan8:amd64 (12.2.0-14) ...
Selecting previously unselected package liblsan0:amd64.
Preparing to unpack .../20-liblsan0_12.2.0-14_amd64.deb ...
Unpacking liblsan0:amd64 (12.2.0-14) ...
Selecting previously unselected package libtsan2:amd64.
Preparing to unpack .../21-libtsan2_12.2.0-14_amd64.deb ...
Unpacking libtsan2:amd64 (12.2.0-14) ...
Selecting previously unselected package libubsan1:amd64.
Preparing to unpack .../22-libubsan1_12.2.0-14_amd64.deb ...
Unpacking libubsan1:amd64 (12.2.0-14) ...
Selecting previously unselected package libquadmath0:amd64.
Preparing to unpack .../23-libquadmath0_12.2.0-14_amd64.deb ...
Unpacking libquadmath0:amd64 (12.2.0-14) ...
Selecting previously unselected package libgcc-12-dev:amd64.
Preparing to unpack .../24-libgcc-12-dev_12.2.0-14_amd64.deb ...
Unpacking libgcc-12-dev:amd64 (12.2.0-14) ...
Selecting previously unselected package gcc-12.
Preparing to unpack .../25-gcc-12_12.2.0-14_amd64.deb ...
Unpacking gcc-12 (12.2.0-14) ...
Selecting previously unselected package gcc.
Preparing to unpack .../26-gcc_4%3a12.2.0-3_amd64.deb ...
Unpacking gcc (4:12.2.0-3) ...
Selecting previously unselected package libc-dev-bin.
Preparing to unpack .../27-libc-dev-bin_2.36-9+deb12u8_amd64.deb ...
Unpacking libc-dev-bin (2.36-9+deb12u8) ...
Selecting previously unselected package linux-libc-dev:amd64.
Preparing to unpack .../28-linux-libc-dev_6.1.112-1_amd64.deb ...
Unpacking linux-libc-dev:amd64 (6.1.112-1) ...
Selecting previously unselected package libcrypt-dev:amd64.
Preparing to unpack .../29-libcrypt-dev_1%3a4.4.33-2_amd64.deb ...
Unpacking libcrypt-dev:amd64 (1:4.4.33-2) ...
Selecting previously unselected package libtirpc-dev:amd64.
Preparing to unpack .../30-libtirpc-dev_1.3.3+ds-1_amd64.deb ...
Unpacking libtirpc-dev:amd64 (1.3.3+ds-1) ...
Selecting previously unselected package libnsl-dev:amd64.
Preparing to unpack .../31-libnsl-dev_1.3.0-2_amd64.deb ...
Unpacking libnsl-dev:amd64 (1.3.0-2) ...
Selecting previously unselected package rpcsvc-proto.
Preparing to unpack .../32-rpcsvc-proto_1.4.3-1_amd64.deb ...
Unpacking rpcsvc-proto (1.4.3-1) ...
Selecting previously unselected package libc6-dev:amd64.
Preparing to unpack .../33-libc6-dev_2.36-9+deb12u8_amd64.deb ...
Unpacking libc6-dev:amd64 (2.36-9+deb12u8) ...
Selecting previously unselected package libstdc++-12-dev:amd64.
Preparing to unpack .../34-libstdc++-12-dev_12.2.0-14_amd64.deb ...
Unpacking libstdc++-12-dev:amd64 (12.2.0-14) ...
Selecting previously unselected package g++-12.
Preparing to unpack .../35-g++-12_12.2.0-14_amd64.deb ...
Unpacking g++-12 (12.2.0-14) ...
Selecting previously unselected package g++.
Preparing to unpack .../36-g++_4%3a12.2.0-3_amd64.deb ...
Unpacking g++ (4:12.2.0-3) ...
Setting up libpsl5:amd64 (0.21.2-1) ...
Setting up wget (1.21.3-1+b2) ...
Setting up binutils-common:amd64 (2.40-2) ...
Setting up linux-libc-dev:amd64 (6.1.112-1) ...
Setting up libctf-nobfd0:amd64 (2.40-2) ...
Setting up libgomp1:amd64 (12.2.0-14) ...
Setting up libjansson4:amd64 (2.14-2) ...
Setting up libtirpc-dev:amd64 (1.3.3+ds-1) ...
Setting up rpcsvc-proto (1.4.3-1) ...
Setting up libmpfr6:amd64 (4.2.0-1) ...
Setting up libquadmath0:amd64 (12.2.0-14) ...
Setting up libmpc3:amd64 (1.3.1-1) ...
Setting up libatomic1:amd64 (12.2.0-14) ...
Setting up libubsan1:amd64 (12.2.0-14) ...
Setting up libnsl-dev:amd64 (1.3.0-2) ...
Setting up libcrypt-dev:amd64 (1:4.4.33-2) ...
Setting up libasan8:amd64 (12.2.0-14) ...
Setting up libtsan2:amd64 (12.2.0-14) ...
Setting up libbinutils:amd64 (2.40-2) ...
Setting up libisl23:amd64 (0.25-1.1) ...
Setting up libc-dev-bin (2.36-9+deb12u8) ...
Setting up libcc1-0:amd64 (12.2.0-14) ...
Setting up liblsan0:amd64 (12.2.0-14) ...
Setting up libitm1:amd64 (12.2.0-14) ...
Setting up libctf0:amd64 (2.40-2) ...
Setting up cpp-12 (12.2.0-14) ...
Setting up libgprofng0:amd64 (2.40-2) ...
Setting up libgcc-12-dev:amd64 (12.2.0-14) ...
Setting up cpp (4:12.2.0-3) ...
Setting up libc6-dev:amd64 (2.36-9+deb12u8) ...
Setting up binutils-x86-64-linux-gnu (2.40-2) ...
Setting up libstdc++-12-dev:amd64 (12.2.0-14) ...
Setting up binutils (2.40-2) ...
Setting up gcc-12 (12.2.0-14) ...
Setting up g++-12 (12.2.0-14) ...
Setting up gcc (4:12.2.0-3) ...
Setting up g++ (4:12.2.0-3) ...
update-alternatives: using /usr/bin/g++ to provide /usr/bin/c++ (c++) in auto mode
Processing triggers for libc-bin (2.36-9+deb12u8) ...
Removing intermediate container fa1a1a50b3b0
 ---> a052677690ca
Step 4/13 : COPY requirements.txt .
 ---> 247b769268e8
Step 5/13 : RUN pip install -r requirements.txt
 ---> Running in 302a97c40139
Collecting backoff==2.2.1 (from -r requirements.txt (line 7))
  Downloading backoff-2.2.1-py3-none-any.whl.metadata (14 kB)
Collecting cachetools==5.3.2 (from -r requirements.txt (line 11))
  Downloading cachetools-5.3.2-py3-none-any.whl.metadata (5.2 kB)
Collecting certifi==2023.7.22 (from -r requirements.txt (line 13))
  Downloading certifi-2023.7.22-py3-none-any.whl.metadata (2.2 kB)
Collecting charset-normalizer==3.3.2 (from -r requirements.txt (line 15))
  Downloading charset_normalizer-3.3.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (33 kB)
Collecting deprecated==1.2.14 (from -r requirements.txt (line 17))
  Downloading Deprecated-1.2.14-py2.py3-none-any.whl.metadata (5.4 kB)
Collecting google-api-core==2.12.0 (from google-api-core[grpc]==2.12.0->-r requirements.txt (line 21))
  Downloading google_api_core-2.12.0-py3-none-any.whl.metadata (2.7 kB)
Collecting google-api-python-client==2.107.0 (from -r requirements.txt (line 26))
  Downloading google_api_python_client-2.107.0-py2.py3-none-any.whl.metadata (6.6 kB)
Collecting google-auth==2.23.4 (from -r requirements.txt (line 28))
  Downloading google_auth-2.23.4-py2.py3-none-any.whl.metadata (4.7 kB)
Collecting google-auth-httplib2==0.1.1 (from -r requirements.txt (line 34))
  Downloading google_auth_httplib2-0.1.1-py2.py3-none-any.whl.metadata (2.1 kB)
Collecting google-cloud-profiler==4.1.0 (from -r requirements.txt (line 38))
  Downloading google-cloud-profiler-4.1.0.tar.gz (32 kB)
  Installing build dependencies: started
  Installing build dependencies: finished with status 'done'
  Getting requirements to build wheel: started
  Getting requirements to build wheel: finished with status 'done'
  Installing backend dependencies: started
  Installing backend dependencies: finished with status 'done'
  Preparing metadata (pyproject.toml): started
  Preparing metadata (pyproject.toml): finished with status 'done'
Collecting google-cloud-trace==1.11.3 (from -r requirements.txt (line 40))
  Downloading google_cloud_trace-1.11.3-py2.py3-none-any.whl.metadata (5.1 kB)
Collecting googleapis-common-protos==1.61.0 (from -r requirements.txt (line 42))
  Downloading googleapis_common_protos-1.61.0-py2.py3-none-any.whl.metadata (1.5 kB)
Collecting grpcio==1.59.2 (from -r requirements.txt (line 47))
  Downloading grpcio-1.59.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (4.0 kB)
Collecting grpcio-health-checking==1.59.2 (from -r requirements.txt (line 54))
  Downloading grpcio_health_checking-1.59.2-py3-none-any.whl.metadata (1.3 kB)
Collecting grpcio-status==1.59.2 (from -r requirements.txt (line 56))
  Downloading grpcio_status-1.59.2-py3-none-any.whl.metadata (1.3 kB)
Collecting httplib2==0.22.0 (from -r requirements.txt (line 58))
  Downloading httplib2-0.22.0-py3-none-any.whl.metadata (2.6 kB)
Collecting idna==3.4 (from -r requirements.txt (line 62))
  Downloading idna-3.4-py3-none-any.whl.metadata (9.8 kB)
Collecting importlib-metadata==6.8.0 (from -r requirements.txt (line 64))
  Downloading importlib_metadata-6.8.0-py3-none-any.whl.metadata (5.1 kB)
Collecting jinja2==3.1.2 (from -r requirements.txt (line 66))
  Downloading Jinja2-3.1.2-py3-none-any.whl.metadata (3.5 kB)
Collecting markupsafe==2.1.3 (from -r requirements.txt (line 68))
  Downloading MarkupSafe-2.1.3-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (2.9 kB)
Collecting opentelemetry-api==1.20.0 (from -r requirements.txt (line 70))
  Downloading opentelemetry_api-1.20.0-py3-none-any.whl.metadata (1.4 kB)
Collecting opentelemetry-distro==0.41b0 (from -r requirements.txt (line 77))
  Downloading opentelemetry_distro-0.41b0-py3-none-any.whl.metadata (1.5 kB)
Collecting opentelemetry-exporter-otlp-proto-common==1.20.0 (from -r requirements.txt (line 79))
  Downloading opentelemetry_exporter_otlp_proto_common-1.20.0-py3-none-any.whl.metadata (1.8 kB)
Collecting opentelemetry-exporter-otlp-proto-grpc==1.20.0 (from -r requirements.txt (line 81))
  Downloading opentelemetry_exporter_otlp_proto_grpc-1.20.0-py3-none-any.whl.metadata (2.4 kB)
Collecting opentelemetry-instrumentation==0.41b0 (from -r requirements.txt (line 83))
  Downloading opentelemetry_instrumentation-0.41b0-py3-none-any.whl.metadata (5.9 kB)
Collecting opentelemetry-instrumentation-grpc==0.41b0 (from -r requirements.txt (line 87))
  Downloading opentelemetry_instrumentation_grpc-0.41b0-py3-none-any.whl.metadata (2.2 kB)
Collecting opentelemetry-proto==1.20.0 (from -r requirements.txt (line 89))
  Downloading opentelemetry_proto-1.20.0-py3-none-any.whl.metadata (2.3 kB)
Collecting opentelemetry-sdk==1.20.0 (from -r requirements.txt (line 93))
  Downloading opentelemetry_sdk-1.20.0-py3-none-any.whl.metadata (1.5 kB)
Collecting opentelemetry-semantic-conventions==0.41b0 (from -r requirements.txt (line 98))
  Downloading opentelemetry_semantic_conventions-0.41b0-py3-none-any.whl.metadata (2.3 kB)
Collecting proto-plus==1.22.3 (from -r requirements.txt (line 102))
  Downloading proto_plus-1.22.3-py3-none-any.whl.metadata (2.2 kB)
Collecting protobuf==4.25.0 (from -r requirements.txt (line 104))
  Downloading protobuf-4.25.0-cp37-abi3-manylinux2014_x86_64.whl.metadata (541 bytes)
Collecting pyasn1==0.5.0 (from -r requirements.txt (line 114))
  Downloading pyasn1-0.5.0-py2.py3-none-any.whl.metadata (8.5 kB)
Collecting pyasn1-modules==0.3.0 (from -r requirements.txt (line 118))
  Downloading pyasn1_modules-0.3.0-py2.py3-none-any.whl.metadata (3.6 kB)
Collecting pyparsing==3.1.1 (from -r requirements.txt (line 120))
  Downloading pyparsing-3.1.1-py3-none-any.whl.metadata (5.1 kB)
Collecting python-json-logger==2.0.7 (from -r requirements.txt (line 122))
  Downloading python_json_logger-2.0.7-py3-none-any.whl.metadata (6.5 kB)
Collecting requests==2.31.0 (from -r requirements.txt (line 124))
  Downloading requests-2.31.0-py3-none-any.whl.metadata (4.6 kB)
Collecting rsa==4.9 (from -r requirements.txt (line 129))
  Downloading rsa-4.9-py3-none-any.whl.metadata (4.2 kB)
Collecting typing-extensions==4.8.0 (from -r requirements.txt (line 131))
  Downloading typing_extensions-4.8.0-py3-none-any.whl.metadata (3.0 kB)
Collecting uritemplate==4.1.1 (from -r requirements.txt (line 133))
  Downloading uritemplate-4.1.1-py2.py3-none-any.whl.metadata (2.9 kB)
Collecting urllib3==2.0.7 (from -r requirements.txt (line 135))
  Downloading urllib3-2.0.7-py3-none-any.whl.metadata (6.6 kB)
Collecting wrapt==1.16.0 (from -r requirements.txt (line 137))
  Downloading wrapt-1.16.0-cp312-cp312-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (6.6 kB)
Collecting zipp==3.17.0 (from -r requirements.txt (line 142))
  Downloading zipp-3.17.0-py3-none-any.whl.metadata (3.7 kB)
Collecting setuptools>=16.0 (from opentelemetry-instrumentation==0.41b0->-r requirements.txt (line 83))
  Using cached setuptools-75.3.0-py3-none-any.whl.metadata (6.9 kB)
Downloading backoff-2.2.1-py3-none-any.whl (15 kB)
Downloading cachetools-5.3.2-py3-none-any.whl (9.3 kB)
Downloading certifi-2023.7.22-py3-none-any.whl (158 kB)
Downloading charset_normalizer-3.3.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (141 kB)
Downloading Deprecated-1.2.14-py2.py3-none-any.whl (9.6 kB)
Downloading google_api_core-2.12.0-py3-none-any.whl (121 kB)
Downloading google_api_python_client-2.107.0-py2.py3-none-any.whl (12.7 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 12.7/12.7 MB 40.7 MB/s eta 0:00:00
Downloading google_auth-2.23.4-py2.py3-none-any.whl (183 kB)
Downloading google_auth_httplib2-0.1.1-py2.py3-none-any.whl (9.3 kB)
Downloading google_cloud_trace-1.11.3-py2.py3-none-any.whl (85 kB)
Downloading googleapis_common_protos-1.61.0-py2.py3-none-any.whl (230 kB)
Downloading grpcio-1.59.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (5.2 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 5.2/5.2 MB 36.9 MB/s eta 0:00:00
Downloading grpcio_health_checking-1.59.2-py3-none-any.whl (17 kB)
Downloading grpcio_status-1.59.2-py3-none-any.whl (14 kB)
Downloading httplib2-0.22.0-py3-none-any.whl (96 kB)
Downloading idna-3.4-py3-none-any.whl (61 kB)
Downloading importlib_metadata-6.8.0-py3-none-any.whl (22 kB)
Downloading Jinja2-3.1.2-py3-none-any.whl (133 kB)
Downloading MarkupSafe-2.1.3-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (28 kB)
Downloading opentelemetry_api-1.20.0-py3-none-any.whl (57 kB)
Downloading opentelemetry_distro-0.41b0-py3-none-any.whl (3.3 kB)
Downloading opentelemetry_exporter_otlp_proto_common-1.20.0-py3-none-any.whl (17 kB)
Downloading opentelemetry_exporter_otlp_proto_grpc-1.20.0-py3-none-any.whl (18 kB)
Downloading opentelemetry_instrumentation-0.41b0-py3-none-any.whl (25 kB)
Downloading opentelemetry_instrumentation_grpc-0.41b0-py3-none-any.whl (26 kB)
Downloading opentelemetry_proto-1.20.0-py3-none-any.whl (50 kB)
Downloading opentelemetry_sdk-1.20.0-py3-none-any.whl (103 kB)
Downloading opentelemetry_semantic_conventions-0.41b0-py3-none-any.whl (26 kB)
Downloading proto_plus-1.22.3-py3-none-any.whl (48 kB)
Downloading protobuf-4.25.0-cp37-abi3-manylinux2014_x86_64.whl (294 kB)
Downloading pyasn1-0.5.0-py2.py3-none-any.whl (83 kB)
Downloading pyasn1_modules-0.3.0-py2.py3-none-any.whl (181 kB)
Downloading pyparsing-3.1.1-py3-none-any.whl (103 kB)
Downloading python_json_logger-2.0.7-py3-none-any.whl (8.1 kB)
Downloading requests-2.31.0-py3-none-any.whl (62 kB)
Downloading rsa-4.9-py3-none-any.whl (34 kB)
Downloading typing_extensions-4.8.0-py3-none-any.whl (31 kB)
Downloading uritemplate-4.1.1-py2.py3-none-any.whl (10 kB)
Downloading urllib3-2.0.7-py3-none-any.whl (124 kB)
Downloading wrapt-1.16.0-cp312-cp312-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (87 kB)
Downloading zipp-3.17.0-py3-none-any.whl (7.4 kB)
Using cached setuptools-75.3.0-py3-none-any.whl (1.3 MB)
Building wheels for collected packages: google-cloud-profiler
  Building wheel for google-cloud-profiler (pyproject.toml): started
  Building wheel for google-cloud-profiler (pyproject.toml): finished with status 'done'
  Created wheel for google-cloud-profiler: filename=google_cloud_profiler-4.1.0-cp312-cp312-linux_x86_64.whl size=761056 sha256=0d07a46de311aa046df46a153ec4322f9ac8291c20cf4c3f62818636ca25ebba
  Stored in directory: /root/.cache/pip/wheels/4c/e9/0e/051a26de1731259c679b0d9546e4a069b9e2adf536bb0566a2
Successfully built google-cloud-profiler
Installing collected packages: zipp, wrapt, urllib3, uritemplate, typing-extensions, setuptools, python-json-logger, pyparsing, pyasn1, protobuf, opentelemetry-semantic-conventions, markupsafe, idna, grpcio, charset-normalizer, certifi, cachetools, backoff, rsa, requests, pyasn1-modules, proto-plus, opentelemetry-proto, jinja2, importlib-metadata, httplib2, grpcio-health-checking, googleapis-common-protos, deprecated, opentelemetry-exporter-otlp-proto-common, opentelemetry-api, grpcio-status, google-auth, opentelemetry-sdk, opentelemetry-instrumentation, google-auth-httplib2, google-api-core, opentelemetry-instrumentation-grpc, opentelemetry-exporter-otlp-proto-grpc, opentelemetry-distro, google-api-python-client, google-cloud-trace, google-cloud-profiler
Successfully installed backoff-2.2.1 cachetools-5.3.2 certifi-2023.7.22 charset-normalizer-3.3.2 deprecated-1.2.14 google-api-core-2.12.0 google-api-python-client-2.107.0 google-auth-2.23.4 google-auth-httplib2-0.1.1 google-cloud-profiler-4.1.0 google-cloud-trace-1.11.3 googleapis-common-protos-1.61.0 grpcio-1.59.2 grpcio-health-checking-1.59.2 grpcio-status-1.59.2 httplib2-0.22.0 idna-3.4 importlib-metadata-6.8.0 jinja2-3.1.2 markupsafe-2.1.3 opentelemetry-api-1.20.0 opentelemetry-distro-0.41b0 opentelemetry-exporter-otlp-proto-common-1.20.0 opentelemetry-exporter-otlp-proto-grpc-1.20.0 opentelemetry-instrumentation-0.41b0 opentelemetry-instrumentation-grpc-0.41b0 opentelemetry-proto-1.20.0 opentelemetry-sdk-1.20.0 opentelemetry-semantic-conventions-0.41b0 proto-plus-1.22.3 protobuf-4.25.0 pyasn1-0.5.0 pyasn1-modules-0.3.0 pyparsing-3.1.1 python-json-logger-2.0.7 requests-2.31.0 rsa-4.9 setuptools-75.3.0 typing-extensions-4.8.0 uritemplate-4.1.1 urllib3-2.0.7 wrapt-1.16.0 zipp-3.17.0
[91mWARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager, possibly rendering your system unusable.It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv. Use the --root-user-action option if you know what you are doing and want to suppress this warning.
[0m[91m
[notice] A new release of pip is available: 24.2 -> 24.3.1
[notice] To update, run: pip install --upgrade pip
[0mRemoving intermediate container 302a97c40139
 ---> 15d01f6e00c9
Step 6/13 : FROM base
 ---> 86b8b6de4ba2
Step 7/13 : ENV PYTHONUNBUFFERED=1
 ---> Running in 9666f2733eb5
Removing intermediate container 9666f2733eb5
 ---> 5eeaf8716fde
Step 8/13 : ENV ENABLE_PROFILER=1
 ---> Running in 142ab0666dfb
Removing intermediate container 142ab0666dfb
 ---> 0d6680c3217f
Step 9/13 : WORKDIR /email_server
 ---> Running in acad366c05ff
Removing intermediate container acad366c05ff
 ---> 049e7665d215
Step 10/13 : COPY --from=builder /usr/local/lib/python3.12/ /usr/local/lib/python3.12/
 ---> 9df428632bb8
Step 11/13 : COPY . .
 ---> 7b31df5081df
Step 12/13 : EXPOSE 8080
 ---> Running in afa8ff2a054c
Removing intermediate container afa8ff2a054c
 ---> ddc643da41b6
Step 13/13 : ENTRYPOINT [ "python", "email_server.py" ]
 ---> Running in 1432948dc2d0
Removing intermediate container 1432948dc2d0
 ---> fdf4fde611f6
Successfully built fdf4fde611f6
Successfully tagged mwanthi/emailservice:latest
[Pipeline] sh
+ docker tag mwanthi/emailservice mwanthi/emailservice:v0.0.1
[Pipeline] sh
+ docker push mwanthi/emailservice:v0.0.1
The push refers to repository [docker.io/mwanthi/emailservice]
80790db702d2: Preparing
a7593188c069: Preparing
cb874e06a97c: Preparing
e2bc26829d40: Preparing
6102c39d73fe: Preparing
462eacda1a69: Preparing
8d853c8add5d: Preparing
462eacda1a69: Waiting
8d853c8add5d: Waiting
e2bc26829d40: Mounted from library/python
6102c39d73fe: Mounted from library/python
cb874e06a97c: Pushed
80790db702d2: Pushed
462eacda1a69: Mounted from library/python
8d853c8add5d: Mounted from library/python
a7593188c069: Pushed
v0.0.1: digest: sha256:9c2c5e9f29dd255ad2b85980ba0598ef6c6bb0987cbdbe498ff53e318376df26 size: 1786
[Pipeline] sh
+ docker push mwanthi/emailservice:latest
The push refers to repository [docker.io/mwanthi/emailservice]
80790db702d2: Preparing
a7593188c069: Preparing
cb874e06a97c: Preparing
e2bc26829d40: Preparing
6102c39d73fe: Preparing
462eacda1a69: Preparing
8d853c8add5d: Preparing
462eacda1a69: Waiting
8d853c8add5d: Waiting
80790db702d2: Layer already exists
6102c39d73fe: Layer already exists
e2bc26829d40: Layer already exists
a7593188c069: Layer already exists
cb874e06a97c: Layer already exists
462eacda1a69: Layer already exists
8d853c8add5d: Layer already exists
latest: digest: sha256:9c2c5e9f29dd255ad2b85980ba0598ef6c6bb0987cbdbe498ff53e318376df26 size: 1786
[Pipeline] sh
+ sed -i  -e s|mwanthi/emailservice:v0.0.1|mwanthi/emailservice:v0.0.1|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/emailservice/emailservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/emailservice:latest
Untagged: mwanthi/emailservice:latest
[Pipeline] sh
+ docker rmi mwanthi/emailservice:v0.0.1
Untagged: mwanthi/emailservice:v0.0.1
Untagged: mwanthi/emailservice@sha256:9c2c5e9f29dd255ad2b85980ba0598ef6c6bb0987cbdbe498ff53e318376df26
Deleted: sha256:fdf4fde611f649665721821ec2fb469ef730201eba8d33b98528244269988738
Deleted: sha256:ddc643da41b6283f299de71c54a8aba80d373f59c5f83d9aa0726c7564b077c4
Deleted: sha256:7b31df5081df2d9ac6714f61a662bcb5f20620bce5017cd7808ef58423395716
Deleted: sha256:2bf582650812705d7e7da4037329297d1d541e2a6c828489e47263246ffb0950
Deleted: sha256:9df428632bb847d7807e515635625b0f9b092a393616ecbbd7f07186cc4fbe73
Deleted: sha256:39ad44f1b409e6befca95c5ca406b4fe4eea79f591cfa933ee06aea462485aef
Deleted: sha256:049e7665d215284049d2061db8e8079b0bd2d3f299194d58cdff3fd909731093
Deleted: sha256:f9cebd31053963766969ff9da7dcb3569c2bd77e47e452dcb0a0c7bcf8a877fe
Deleted: sha256:0d6680c3217fdb2a2b916c218bafd574ae70890fae86f99d0abdf6c81cb44f74
Deleted: sha256:5eeaf8716fdebabb12572b099f05855233fda46efcd52385f4da32301f139363
[Pipeline] sh
+ docker image prune -f
Deleted Images:
deleted: sha256:15d01f6e00c9fc9d5081509bf0e0b7d9126b2bb7c64a80d5dac8188191a0f3d6
deleted: sha256:7296a0828ce7b42b656a86db41051f7723c65e71285952aef44598dd121c6a25
deleted: sha256:247b769268e8e76185999f299d9610b3c89e3ef6cb56886886175ec33432c8d7
deleted: sha256:6778feb1e9d7d89d02fc2fa6b2d4c433add3179ee0849cd5e4c7a3011dfcd768
deleted: sha256:a052677690cac906d7a0fe3e36f84cd1663018207a9ad29caa5bef02e3bf3f49
deleted: sha256:d218d1d75e85e9fe46826e1c41eb76bddd02bf1cb2f0e8831e1083a740b44edd
untagged: node@sha256:2d07db07a2df6830718ae2a47db6fedce6745f5bcd174c398f2acdda90a11c03
deleted: sha256:45a59611ca84e7fa7e39413f7a657afd43e2b71b8d6cb3cb722d97ffc842decb
deleted: sha256:5224d953fb6159064b9b661e6ea7dda03b4b8ab8eceea889cddb0681220b5322
deleted: sha256:066954302d87006fb52541c44830d87caed51a4d3f60227077cf035619255889
deleted: sha256:9561d1ac6ce7491afee33934a225d0b100cdc011fcd45274b98425090dae4bac
deleted: sha256:63ca1fbb43ae5034640e5e6cb3e083e05c290072c5366fcaa9d62435a4cced85

Total reclaimed space: 542.5MB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] echo
Tracking and building frontend service...
[Pipeline] sh
+ echo frontend
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Building and Pushing frontend image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/13f99b4b-525b-4f7f-919f-350269bafc15/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ awk -F : {print $3}
+ grep image: mwanthi/frontend:[^[:space:]]* /home/ubuntu/workspace/microservices-build/kubernetes-manifests/frontend/frontend.yaml
+ awk {gsub(/^v/, ""); print}
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app/src/frontend
[Pipeline] {
[Pipeline] sh
+ docker build --no-cache -t mwanthi/frontend .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  4.509MB

Step 1/15 : FROM golang:1.23.1-alpine@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06 AS builder
docker.io/library/golang:1.23.1-alpine@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06: Pulling from library/golang
43c4264eed91: Pulling fs layer
ab19dfae90ef: Pulling fs layer
e7bff916ab0c: Pulling fs layer
78cee99375e3: Pulling fs layer
4f4fb700ef54: Pulling fs layer
78cee99375e3: Waiting
4f4fb700ef54: Waiting
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
Step 2/15 : WORKDIR /src
 ---> Running in 8206be0356a7
Removing intermediate container 8206be0356a7
 ---> e2029bf225ea
Step 3/15 : COPY go.mod go.sum ./
 ---> d3af1f70992b
Step 4/15 : RUN go mod download
 ---> Running in 5dfa6560e226
Removing intermediate container 5dfa6560e226
 ---> 9e0c99919ad4
Step 5/15 : COPY . .
 ---> cbec78c952a6
Step 6/15 : ARG SKAFFOLD_GO_GCFLAGS
 ---> Running in d24785e5900d
Removing intermediate container d24785e5900d
 ---> bfe217828e9c
Step 7/15 : RUN CGO_ENABLED=0 GOOS=linux go build -gcflags="${SKAFFOLD_GO_GCFLAGS}" -o /go/bin/frontend .
 ---> Running in f3d30a05a9de
Removing intermediate container f3d30a05a9de
 ---> b74b983feb14
Step 8/15 : FROM scratch
 ---> 
Step 9/15 : WORKDIR /src
 ---> Running in 34b853404b64
Removing intermediate container 34b853404b64
 ---> a66e9013f276
Step 10/15 : COPY --from=builder /go/bin/frontend /src/server
 ---> 896283b45c2a
Step 11/15 : COPY ./templates ./templates
 ---> cbbaaf39c567
Step 12/15 : COPY ./static ./static
 ---> f17b939f11d0
Step 13/15 : ENV GOTRACEBACK=single
 ---> Running in c38b7046d613
Removing intermediate container c38b7046d613
 ---> b42b8865ecc3
Step 14/15 : EXPOSE 8080
 ---> Running in cd8386e42020
Removing intermediate container cd8386e42020
 ---> 4b93daba9ee3
Step 15/15 : ENTRYPOINT ["/src/server"]
 ---> Running in d7b4af9c08bb
Removing intermediate container d7b4af9c08bb
 ---> 5d8b8853c17e
Successfully built 5d8b8853c17e
Successfully tagged mwanthi/frontend:latest
[Pipeline] sh
+ docker tag mwanthi/frontend mwanthi/frontend:v0.0.1
[Pipeline] sh
+ docker push mwanthi/frontend:v0.0.1
The push refers to repository [docker.io/mwanthi/frontend]
3bfa807c9e97: Preparing
fd50f3e6cd29: Preparing
a12ec7f8f6be: Preparing
1cd8f8c17ca5: Preparing
1cd8f8c17ca5: Pushed
fd50f3e6cd29: Pushed
3bfa807c9e97: Pushed
a12ec7f8f6be: Pushed
v0.0.1: digest: sha256:d681da26b59b9f7357cc273c508aa6a94ff8b594f558e0ff86cfaf6b4e401413 size: 1154
[Pipeline] sh
+ docker push mwanthi/frontend:latest
The push refers to repository [docker.io/mwanthi/frontend]
3bfa807c9e97: Preparing
fd50f3e6cd29: Preparing
a12ec7f8f6be: Preparing
1cd8f8c17ca5: Preparing
3bfa807c9e97: Layer already exists
a12ec7f8f6be: Layer already exists
fd50f3e6cd29: Layer already exists
1cd8f8c17ca5: Layer already exists
latest: digest: sha256:d681da26b59b9f7357cc273c508aa6a94ff8b594f558e0ff86cfaf6b4e401413 size: 1154
[Pipeline] sh
+ sed -i  -e s|mwanthi/frontend:v0.0.1|mwanthi/frontend:v0.0.1|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/frontend/frontend.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/frontend:latest
Untagged: mwanthi/frontend:latest
[Pipeline] sh
+ docker rmi mwanthi/frontend:v0.0.1
Untagged: mwanthi/frontend:v0.0.1
Untagged: mwanthi/frontend@sha256:d681da26b59b9f7357cc273c508aa6a94ff8b594f558e0ff86cfaf6b4e401413
Deleted: sha256:5d8b8853c17e84aa0f5de0ebb4d5037d1f815729b9c0cb0446f3a34bc0b9a86e
Deleted: sha256:4b93daba9ee35e14efc753b5d1b669dd985b62fb1a50c793c64fe72618b252cf
Deleted: sha256:b42b8865ecc391460b41183f5f18680797e559ad51c5453b0f8c46b5d746460b
Deleted: sha256:f17b939f11d0a1dd6969d5f7082c3dc353f37b579e33ea4d1a0224707a559562
Deleted: sha256:af0104fe14b01eecd3e6daeb514d08e85eb084d8fdd08d1fed9fea713412366a
Deleted: sha256:cbbaaf39c567a8a5f4a00ad09cbc76b399c0dc97e84cc0d6a8bc75a02d5234bd
Deleted: sha256:e51a03c41c8ef820eb4a6296fe6dcc7983ea93f9e35cb5fdadb880db314dac92
Deleted: sha256:896283b45c2a238de9f95d28d89a3de96abba0a9642654f61d969b37ac769f08
Deleted: sha256:4359906644a86b87d1ecaecd280a5f8b6118962d88b2fc17780d78c0a7ec9f4d
Deleted: sha256:a66e9013f276031a2ed6c246eeed6c7fe2a8fd851dde1a688ef747c1b295f05f
Deleted: sha256:1cd8f8c17ca56d3e4ec5ae7650242feaac07f8d378c555c9ef874e9dd00cd299
[Pipeline] sh
+ docker image prune -f
Deleted Images:
untagged: python@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26
deleted: sha256:86b8b6de4ba2edaa00b6721a7d77a19dc0b20642af20f772b71152fda8d5a3a8
deleted: sha256:06cd4d7df090c22215821a922931f3b2063b7540b1a380407c764a102b128491
deleted: sha256:74a2d6d826bd4906ec5ea1b9b11e1a01f5d2053a86165d59badf7a3677741847
deleted: sha256:0e0d8c7ac030d9d8fad72239164c1f2fde61d0590c35a4c07c4a2f3aa027baaf
deleted: sha256:8d853c8add5d1e7b0aafc4b68a3d9fb8e7a0da27970c2acf831fe63be4a0cd2c
deleted: sha256:b74b983feb1499af653f5dcdf22b2e8aeff75077310516595ee970e0bd479954
deleted: sha256:e26752d8b766f055e817f7d3b175ee32b45a99e846676e3bfc09b1dec59531f7
deleted: sha256:bfe217828e9c8f697b592de4c244c9bd7b814644512d45432e91598ef5e3567e
deleted: sha256:cbec78c952a6bd0377aad68d654b90d8fa976788986cbfdb04df942fd9138dd6
deleted: sha256:4e3640bce5f4939974ad4a45395541b0c14ee8f6726fcf8037e6bd850f2a76dd
deleted: sha256:9e0c99919ad40e56761dfdf5096777c541e14a407357c3919c0a055825de602c
deleted: sha256:641cbd37f8ac5884541034dd1530a06db589e72f5261fc48c90381d20a4bb377
deleted: sha256:d3af1f70992b1a7eb738cb15a41f1fcd4cb45ab0d13a185280da9a6550cdc148
deleted: sha256:b146896e5297886d41289e06b445970d254aa1cf34f74769f10a31c30045bb40
deleted: sha256:e2029bf225ea4f9c1dd8acb7e7dad5429a0cb80d2484d10230346bb03e4944c0
deleted: sha256:b9ae9cf399d77bbfdb3f6dd93b24397250a2caca7fdd328ff079a0fd3a4ee6fc

Total reclaimed space: 993.6MB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] echo
Tracking and building loadgenerator service...
[Pipeline] sh
+ echo loadgenerator
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Building and Pushing loadgenerator image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/fde64607-3831-43d5-b444-674e29769275/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ grep image: mwanthi/loadgenerator:[^[:space:]]* /home/ubuntu/workspace/microservices-build/kubernetes-manifests/loadgenerator/loadgenerator.yaml
+ awk {gsub(/^v/, ""); print}
+ awk -F : {print $3}
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app/src/loadgenerator
[Pipeline] {
[Pipeline] sh
+ docker build --no-cache -t mwanthi/loadgenerator .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  9.216kB

Step 1/10 : FROM python:3.12.6-slim@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26 AS base
docker.io/library/python:3.12.6-slim@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26: Pulling from library/python
302e3ee49805: Pulling fs layer
699edf835b1b: Pulling fs layer
417a872b7725: Pulling fs layer
9795987f6d21: Pulling fs layer
9795987f6d21: Waiting
699edf835b1b: Verifying Checksum
699edf835b1b: Download complete
417a872b7725: Verifying Checksum
417a872b7725: Download complete
302e3ee49805: Verifying Checksum
302e3ee49805: Download complete
9795987f6d21: Verifying Checksum
9795987f6d21: Download complete
302e3ee49805: Pull complete
699edf835b1b: Pull complete
417a872b7725: Pull complete
9795987f6d21: Pull complete
Digest: sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26
Status: Downloaded newer image for python:3.12.6-slim@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26
 ---> 86b8b6de4ba2
Step 2/10 : FROM base AS builder
 ---> 86b8b6de4ba2
Step 3/10 : COPY requirements.txt .
 ---> 3b6877d62031
Step 4/10 : RUN pip install --prefix="/install" -r requirements.txt
 ---> Running in 4471cbefcbec
Collecting blinker==1.8.2 (from -r requirements.txt (line 7))
  Downloading blinker-1.8.2-py3-none-any.whl.metadata (1.6 kB)
Collecting brotli==1.1.0 (from -r requirements.txt (line 9))
  Downloading Brotli-1.1.0-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (5.5 kB)
Collecting certifi==2024.8.30 (from -r requirements.txt (line 11))
  Downloading certifi-2024.8.30-py3-none-any.whl.metadata (2.2 kB)
Collecting charset-normalizer==3.4.0 (from -r requirements.txt (line 15))
  Downloading charset_normalizer-3.4.0-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (34 kB)
Collecting click==8.1.7 (from -r requirements.txt (line 17))
  Downloading click-8.1.7-py3-none-any.whl.metadata (3.0 kB)
Collecting configargparse==1.7 (from -r requirements.txt (line 19))
  Downloading ConfigArgParse-1.7-py3-none-any.whl.metadata (23 kB)
Collecting faker==30.8.0 (from -r requirements.txt (line 21))
  Downloading Faker-30.8.0-py3-none-any.whl.metadata (15 kB)
Collecting flask==3.0.3 (from -r requirements.txt (line 23))
  Downloading flask-3.0.3-py3-none-any.whl.metadata (3.2 kB)
Collecting flask-cors==5.0.0 (from -r requirements.txt (line 28))
  Downloading Flask_Cors-5.0.0-py2.py3-none-any.whl.metadata (5.5 kB)
Collecting flask-login==0.6.3 (from -r requirements.txt (line 30))
  Downloading Flask_Login-0.6.3-py3-none-any.whl.metadata (5.8 kB)
Collecting gevent==24.10.3 (from -r requirements.txt (line 32))
  Downloading gevent-24.10.3-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (13 kB)
Collecting geventhttpclient==2.3.1 (from -r requirements.txt (line 36))
  Downloading geventhttpclient-2.3.1-cp312-cp312-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (9.7 kB)
Collecting greenlet==3.1.1 (from -r requirements.txt (line 38))
  Downloading greenlet-3.1.1-cp312-cp312-manylinux_2_24_x86_64.manylinux_2_28_x86_64.whl.metadata (3.8 kB)
Collecting idna==3.10 (from -r requirements.txt (line 40))
  Downloading idna-3.10-py3-none-any.whl.metadata (10 kB)
Collecting itsdangerous==2.2.0 (from -r requirements.txt (line 42))
  Downloading itsdangerous-2.2.0-py3-none-any.whl.metadata (1.9 kB)
Collecting jinja2==3.1.4 (from -r requirements.txt (line 44))
  Downloading jinja2-3.1.4-py3-none-any.whl.metadata (2.6 kB)
Collecting locust==2.32.0 (from -r requirements.txt (line 46))
  Downloading locust-2.32.0-py3-none-any.whl.metadata (7.9 kB)
Collecting markupsafe==3.0.2 (from -r requirements.txt (line 48))
  Downloading MarkupSafe-3.0.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (4.0 kB)
Collecting msgpack==1.1.0 (from -r requirements.txt (line 52))
  Downloading msgpack-1.1.0-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (8.4 kB)
Collecting psutil==6.1.0 (from -r requirements.txt (line 54))
  Downloading psutil-6.1.0-cp36-abi3-manylinux_2_12_x86_64.manylinux2010_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (22 kB)
Collecting python-dateutil==2.9.0.post0 (from -r requirements.txt (line 56))
  Downloading python_dateutil-2.9.0.post0-py2.py3-none-any.whl.metadata (8.4 kB)
Collecting pyzmq==26.2.0 (from -r requirements.txt (line 58))
  Downloading pyzmq-26.2.0-cp312-cp312-manylinux_2_28_x86_64.whl.metadata (6.2 kB)
Collecting requests==2.32.3 (from -r requirements.txt (line 60))
  Downloading requests-2.32.3-py3-none-any.whl.metadata (4.6 kB)
Collecting six==1.16.0 (from -r requirements.txt (line 62))
  Downloading six-1.16.0-py2.py3-none-any.whl.metadata (1.8 kB)
Collecting typing-extensions==4.12.2 (from -r requirements.txt (line 64))
  Downloading typing_extensions-4.12.2-py3-none-any.whl.metadata (3.0 kB)
Collecting urllib3==2.2.3 (from -r requirements.txt (line 66))
  Downloading urllib3-2.2.3-py3-none-any.whl.metadata (6.5 kB)
Collecting werkzeug==3.0.6 (from -r requirements.txt (line 70))
  Downloading werkzeug-3.0.6-py3-none-any.whl.metadata (3.7 kB)
Collecting zope-event==5.0 (from -r requirements.txt (line 75))
  Downloading zope.event-5.0-py3-none-any.whl.metadata (4.4 kB)
Collecting zope-interface==7.1.1 (from -r requirements.txt (line 77))
  Downloading zope.interface-7.1.1-cp312-cp312-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (44 kB)
Collecting setuptools (from zope-event==5.0->-r requirements.txt (line 75))
  Downloading setuptools-75.3.0-py3-none-any.whl.metadata (6.9 kB)
Downloading blinker-1.8.2-py3-none-any.whl (9.5 kB)
Downloading Brotli-1.1.0-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (2.9 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.9/2.9 MB 85.4 MB/s eta 0:00:00
Downloading certifi-2024.8.30-py3-none-any.whl (167 kB)
Downloading charset_normalizer-3.4.0-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (143 kB)
Downloading click-8.1.7-py3-none-any.whl (97 kB)
Downloading ConfigArgParse-1.7-py3-none-any.whl (25 kB)
Downloading Faker-30.8.0-py3-none-any.whl (1.8 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.8/1.8 MB 51.6 MB/s eta 0:00:00
Downloading flask-3.0.3-py3-none-any.whl (101 kB)
Downloading Flask_Cors-5.0.0-py2.py3-none-any.whl (14 kB)
Downloading Flask_Login-0.6.3-py3-none-any.whl (17 kB)
Downloading gevent-24.10.3-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (6.8 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 6.8/6.8 MB 111.5 MB/s eta 0:00:00
Downloading geventhttpclient-2.3.1-cp312-cp312-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (113 kB)
Downloading greenlet-3.1.1-cp312-cp312-manylinux_2_24_x86_64.manylinux_2_28_x86_64.whl (613 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 613.1/613.1 kB 32.9 MB/s eta 0:00:00
Downloading idna-3.10-py3-none-any.whl (70 kB)
Downloading itsdangerous-2.2.0-py3-none-any.whl (16 kB)
Downloading jinja2-3.1.4-py3-none-any.whl (133 kB)
Downloading locust-2.32.0-py3-none-any.whl (1.2 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.2/1.2 MB 50.3 MB/s eta 0:00:00
Downloading MarkupSafe-3.0.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (23 kB)
Downloading msgpack-1.1.0-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (401 kB)
Downloading psutil-6.1.0-cp36-abi3-manylinux_2_12_x86_64.manylinux2010_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (287 kB)
Downloading python_dateutil-2.9.0.post0-py2.py3-none-any.whl (229 kB)
Downloading pyzmq-26.2.0-cp312-cp312-manylinux_2_28_x86_64.whl (860 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 860.6/860.6 kB 31.3 MB/s eta 0:00:00
Downloading requests-2.32.3-py3-none-any.whl (64 kB)
Downloading six-1.16.0-py2.py3-none-any.whl (11 kB)
Downloading typing_extensions-4.12.2-py3-none-any.whl (37 kB)
Downloading urllib3-2.2.3-py3-none-any.whl (126 kB)
Downloading werkzeug-3.0.6-py3-none-any.whl (227 kB)
Downloading zope.event-5.0-py3-none-any.whl (6.8 kB)
Downloading zope.interface-7.1.1-cp312-cp312-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (264 kB)
Downloading setuptools-75.3.0-py3-none-any.whl (1.3 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.3/1.3 MB 62.0 MB/s eta 0:00:00
Installing collected packages: brotli, urllib3, typing-extensions, six, setuptools, pyzmq, psutil, msgpack, markupsafe, itsdangerous, idna, greenlet, configargparse, click, charset-normalizer, certifi, blinker, zope-interface, zope-event, werkzeug, requests, python-dateutil, jinja2, gevent, flask, faker, geventhttpclient, flask-login, flask-cors, locust
Successfully installed blinker-1.8.2 brotli-1.1.0 certifi-2024.8.30 charset-normalizer-3.4.0 click-8.1.7 configargparse-1.7 faker-30.8.0 flask-3.0.3 flask-cors-5.0.0 flask-login-0.6.3 gevent-24.10.3 geventhttpclient-2.3.1 greenlet-3.1.1 idna-3.10 itsdangerous-2.2.0 jinja2-3.1.4 locust-2.32.0 markupsafe-3.0.2 msgpack-1.1.0 psutil-6.1.0 python-dateutil-2.9.0.post0 pyzmq-26.2.0 requests-2.32.3 setuptools-75.3.0 six-1.16.0 typing-extensions-4.12.2 urllib3-2.2.3 werkzeug-3.0.6 zope-event-5.0 zope-interface-7.1.1
[91mWARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager, possibly rendering your system unusable.It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv. Use the --root-user-action option if you know what you are doing and want to suppress this warning.
[0m[91m
[notice] A new release of pip is available: 24.2 -> 24.3.1
[notice] To update, run: pip install --upgrade pip
[0mRemoving intermediate container 4471cbefcbec
 ---> 07bf42fee180
Step 5/10 : FROM base
 ---> 86b8b6de4ba2
Step 6/10 : WORKDIR /loadgen
 ---> Running in fb41bc5f43fc
Removing intermediate container fb41bc5f43fc
 ---> ce0844451d62
Step 7/10 : COPY --from=builder /install /usr/local
 ---> a13d7feb903e
Step 8/10 : COPY locustfile.py .
 ---> 1fda68473611
Step 9/10 : ENV GEVENT_SUPPORT=True
 ---> Running in 78fbc51aecfb
Removing intermediate container 78fbc51aecfb
 ---> c6a4f7772095
Step 10/10 : ENTRYPOINT locust --host="http://${FRONTEND_ADDR}" --headless -u "${USERS:-10}" 2>&1
 ---> Running in c3a291616690
Removing intermediate container c3a291616690
 ---> 0e9354a96015
Successfully built 0e9354a96015
Successfully tagged mwanthi/loadgenerator:latest
[Pipeline] sh
+ docker tag mwanthi/loadgenerator mwanthi/loadgenerator:v0.0.1
[Pipeline] sh
+ docker push mwanthi/loadgenerator:v0.0.1
The push refers to repository [docker.io/mwanthi/loadgenerator]
79c78ce527e6: Preparing
d729ce13fdb8: Preparing
0e2cf4570f56: Preparing
e2bc26829d40: Preparing
6102c39d73fe: Preparing
462eacda1a69: Preparing
8d853c8add5d: Preparing
462eacda1a69: Waiting
8d853c8add5d: Waiting
6102c39d73fe: Mounted from mwanthi/emailservice
e2bc26829d40: Mounted from mwanthi/emailservice
0e2cf4570f56: Pushed
79c78ce527e6: Pushed
462eacda1a69: Mounted from mwanthi/emailservice
8d853c8add5d: Mounted from mwanthi/emailservice
d729ce13fdb8: Pushed
v0.0.1: digest: sha256:ea98d429e8e99e568d09636dce8bc23ca1b78959c4b8e3610ef7f507817cc990 size: 1785
[Pipeline] sh
+ docker push mwanthi/loadgenerator:latest
The push refers to repository [docker.io/mwanthi/loadgenerator]
79c78ce527e6: Preparing
d729ce13fdb8: Preparing
0e2cf4570f56: Preparing
e2bc26829d40: Preparing
6102c39d73fe: Preparing
462eacda1a69: Preparing
8d853c8add5d: Preparing
462eacda1a69: Waiting
8d853c8add5d: Waiting
e2bc26829d40: Layer already exists
6102c39d73fe: Layer already exists
d729ce13fdb8: Layer already exists
79c78ce527e6: Layer already exists
0e2cf4570f56: Layer already exists
8d853c8add5d: Layer already exists
462eacda1a69: Layer already exists
latest: digest: sha256:ea98d429e8e99e568d09636dce8bc23ca1b78959c4b8e3610ef7f507817cc990 size: 1785
[Pipeline] sh
+ sed -i  -e s|mwanthi/loadgenerator:v0.0.1|mwanthi/loadgenerator:v0.0.1|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/loadgenerator/loadgenerator.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/loadgenerator:latest
Untagged: mwanthi/loadgenerator:latest
[Pipeline] sh
+ docker rmi mwanthi/loadgenerator:v0.0.1
Untagged: mwanthi/loadgenerator:v0.0.1
Untagged: mwanthi/loadgenerator@sha256:ea98d429e8e99e568d09636dce8bc23ca1b78959c4b8e3610ef7f507817cc990
Deleted: sha256:0e9354a96015cdd96091622f7535af2913faa480c6d3828fd973d433142f28af
Deleted: sha256:c6a4f777209530dfec7ffaa1dfad3faf05a912469d102e47e636961e182d74bf
Deleted: sha256:1fda684736114b541ae36eda13295a7ae8d9f7710c74f8323712aaa7a72ea2a8
Deleted: sha256:aa5017001071f20c547ec8fc2746b77b413b3a85c55a28d11bc595f719e5543b
Deleted: sha256:a13d7feb903e92b02b21baf758bf48e3918c42bec47559c89b85a54f3d3d25b4
Deleted: sha256:149d10fbf38886008a0610aea04d9128608725cec2f9d0b805a0670a019bbeba
Deleted: sha256:ce0844451d629a9e00b1aa88d5df6c2150b6dd2a0d23bbcf58609cd179b6b1ab
Deleted: sha256:f194a5d6bf15f32a6c330a96aa1e263871a2e49d495bb95f08acc3d20a9e429c
[Pipeline] sh
+ docker image prune -f
Deleted Images:
untagged: golang@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06
deleted: sha256:b5ada884192f173018fcb39688bd70545669ab105941231067ea5dbed4ac6914
deleted: sha256:2968ff6a64392cda70b3e2cb5d6e62723bfdc18fe68b46382c971bee002890a2
deleted: sha256:768a08d8d838830bce342fdf82d2051ad375b9a575cb6cb685f8841bc16f5ae2
deleted: sha256:7c37ab7540e48469f2843766943fb1f5b838efe35a1e500268f45f1b6ba88942
deleted: sha256:db287705205f639bdfff0f98a53c5b40608826ee5ab2b1180bcf22eec319953c
deleted: sha256:63ca1fbb43ae5034640e5e6cb3e083e05c290072c5366fcaa9d62435a4cced85
deleted: sha256:07bf42fee18079cc5d171a9610bbac15def81d6b73aef348f36ed6ed9231939f
deleted: sha256:16844084bed7d1fae2aa4a0bdd5949b6a71fcb96e73b3444e1cfc71c856ac7e5
deleted: sha256:3b6877d6203118d9da9521a0a9f442c11eba9903be928afe8ab253581e517c41
deleted: sha256:beff50fba193cb9a70832050e5e2ba14d00c20c473f821dbeb3f9efc1dee4e2d

Total reclaimed space: 355MB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] echo
Tracking and building paymentservice service...
[Pipeline] sh
+ echo paymentservice
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Building and Pushing paymentservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/6f3a851f-757a-48bb-b639-661feaecafad/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ grep image: mwanthi/paymentservice:[^[:space:]]* /home/ubuntu/workspace/microservices-build/kubernetes-manifests/paymentservice/paymentservice.yaml
+ awk {gsub(/^v/, ""); print}
+ awk -F : {print $3}
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app/src/paymentservice
[Pipeline] {
[Pipeline] sh
+ docker build --no-cache -t mwanthi/paymentservice .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon    235kB

Step 1/12 : FROM node:20.17.0-alpine@sha256:2d07db07a2df6830718ae2a47db6fedce6745f5bcd174c398f2acdda90a11c03 AS builder
docker.io/library/node:20.17.0-alpine@sha256:2d07db07a2df6830718ae2a47db6fedce6745f5bcd174c398f2acdda90a11c03: Pulling from library/node
43c4264eed91: Pulling fs layer
c36270121b0c: Pulling fs layer
842cd80f9366: Pulling fs layer
737da86e5e86: Pulling fs layer
737da86e5e86: Waiting
842cd80f9366: Verifying Checksum
842cd80f9366: Download complete
43c4264eed91: Verifying Checksum
43c4264eed91: Download complete
43c4264eed91: Pull complete
c36270121b0c: Verifying Checksum
c36270121b0c: Download complete
737da86e5e86: Verifying Checksum
737da86e5e86: Download complete
c36270121b0c: Pull complete
842cd80f9366: Pull complete
737da86e5e86: Pull complete
Digest: sha256:2d07db07a2df6830718ae2a47db6fedce6745f5bcd174c398f2acdda90a11c03
Status: Downloaded newer image for node:20.17.0-alpine@sha256:2d07db07a2df6830718ae2a47db6fedce6745f5bcd174c398f2acdda90a11c03
 ---> 45a59611ca84
Step 2/12 : RUN apk add --update --no-cache     python3     make     g++
 ---> Running in eb84566a3989
fetch https://dl-cdn.alpinelinux.org/alpine/v3.20/main/x86_64/APKINDEX.tar.gz
fetch https://dl-cdn.alpinelinux.org/alpine/v3.20/community/x86_64/APKINDEX.tar.gz
(1/29) Installing libstdc++-dev (13.2.1_git20240309-r0)
(2/29) Installing jansson (2.14-r4)
(3/29) Installing zstd-libs (1.5.6-r0)
(4/29) Installing binutils (2.42-r0)
(5/29) Installing libgomp (13.2.1_git20240309-r0)
(6/29) Installing libatomic (13.2.1_git20240309-r0)
(7/29) Installing gmp (6.3.0-r1)
(8/29) Installing isl26 (0.26-r1)
(9/29) Installing mpfr4 (4.2.1-r0)
(10/29) Installing mpc1 (1.3.1-r1)
(11/29) Installing gcc (13.2.1_git20240309-r0)
(12/29) Installing musl-dev (1.2.5-r0)
(13/29) Installing g++ (13.2.1_git20240309-r0)
(14/29) Installing make (4.4.1-r2)
(15/29) Installing libbz2 (1.0.8-r6)
(16/29) Installing libexpat (2.6.3-r0)
(17/29) Installing libffi (3.4.6-r0)
(18/29) Installing gdbm (1.23-r1)
(19/29) Installing xz-libs (5.6.2-r0)
(20/29) Installing mpdecimal (4.0.0-r0)
(21/29) Installing ncurses-terminfo-base (6.4_p20240420-r1)
(22/29) Installing libncursesw (6.4_p20240420-r1)
(23/29) Installing libpanelw (6.4_p20240420-r1)
(24/29) Installing readline (8.2.10-r0)
(25/29) Installing sqlite-libs (3.45.3-r1)
(26/29) Installing python3 (3.12.7-r0)
(27/29) Installing python3-pycache-pyc0 (3.12.7-r0)
(28/29) Installing pyc (3.12.7-r0)
(29/29) Installing python3-pyc (3.12.7-r0)
Executing busybox-1.36.1-r29.trigger
OK: 255 MiB in 45 packages
Removing intermediate container eb84566a3989
 ---> 183db401887a
Step 3/12 : WORKDIR /usr/src/app
 ---> Running in f8464b51ffcc
Removing intermediate container f8464b51ffcc
 ---> 667091fea171
Step 4/12 : COPY package*.json ./
 ---> 0bcaa9e0ebdd
Step 5/12 : RUN npm install --only=production
 ---> Running in ca32867a60d8
[91mnpm warn config only Use `--omit=dev` to omit dev dependencies from the install.
[0m[91mnpm warn deprecated @opentelemetry/exporter-otlp-grpc@0.26.0: Please use trace and metric specific exporters @opentelemetry/exporter-trace-otlp-grpc and @opentelemetry/exporter-metrics-otlp-grpc
[0m[91mnpm warn deprecated @opentelemetry/api-metrics@0.26.0: Please use @opentelemetry/api >= 1.3.0
[0m[91mnpm warn deprecated @opentelemetry/exporter-otlp-http@0.26.0: Please use trace and metric specific exporters @opentelemetry/exporter-trace-otlp-http and @opentelemetry/exporter-metrics-otlp-http
[0m[91mnpm warn deprecated @opentelemetry/sdk-metrics-base@0.26.0: Please use @opentelemetry/sdk-metrics
[0m
added 260 packages, and audited 261 packages in 18s

20 packages are looking for funding
  run `npm fund` for details

1 moderate severity vulnerability

To address all issues, run:
  npm audit fix

Run `npm audit` for details.
[91mnpm notice
npm notice New minor version of npm available! 10.8.2 -> 10.9.0
npm notice Changelog: https://github.com/npm/cli/releases/tag/v10.9.0
npm notice To update run: npm install -g npm@10.9.0
npm notice
[0mRemoving intermediate container ca32867a60d8
 ---> 46cf021a968d
Step 6/12 : FROM alpine:3.20.3@sha256:beefdbd8a1da6d2915566fde36db9db0b524eb737fc57cd1367effd16dc0d06d
docker.io/library/alpine:3.20.3@sha256:beefdbd8a1da6d2915566fde36db9db0b524eb737fc57cd1367effd16dc0d06d: Pulling from library/alpine
43c4264eed91: Already exists
Digest: sha256:beefdbd8a1da6d2915566fde36db9db0b524eb737fc57cd1367effd16dc0d06d
Status: Downloaded newer image for alpine:3.20.3@sha256:beefdbd8a1da6d2915566fde36db9db0b524eb737fc57cd1367effd16dc0d06d
 ---> 91ef0af61f39
Step 7/12 : RUN apk add --no-cache nodejs
 ---> Running in c97ae3f4acd7
fetch https://dl-cdn.alpinelinux.org/alpine/v3.20/main/x86_64/APKINDEX.tar.gz
fetch https://dl-cdn.alpinelinux.org/alpine/v3.20/community/x86_64/APKINDEX.tar.gz
(1/11) Installing ca-certificates (20240705-r0)
(2/11) Installing libgcc (13.2.1_git20240309-r0)
(3/11) Installing libstdc++ (13.2.1_git20240309-r0)
(4/11) Installing ada-libs (2.7.8-r0)
(5/11) Installing libbase64 (0.5.2-r0)
(6/11) Installing brotli-libs (1.1.0-r2)
(7/11) Installing c-ares (1.33.1-r0)
(8/11) Installing icu-data-en (74.2-r0)
Executing icu-data-en-74.2-r0.post-install
[91m*
* If you need ICU with non-English locales and legacy charset support, install
* package icu-data-full.
*
[0m(9/11) Installing icu-libs (74.2-r0)
(10/11) Installing nghttp2-libs (1.62.1-r0)
(11/11) Installing nodejs (20.15.1-r0)
Executing busybox-1.36.1-r29.trigger
Executing ca-certificates-20240705-r0.trigger
OK: 61 MiB in 25 packages
Removing intermediate container c97ae3f4acd7
 ---> 11a7a0602322
Step 8/12 : WORKDIR /usr/src/app
 ---> Running in 39589fc30a88
Removing intermediate container 39589fc30a88
 ---> 69d0bf798993
Step 9/12 : COPY --from=builder /usr/src/app/node_modules ./node_modules
 ---> 60df2b904230
Step 10/12 : COPY . .
 ---> b7fbaa4ff657
Step 11/12 : EXPOSE 50051
 ---> Running in a8672946b809
Removing intermediate container a8672946b809
 ---> b39bf8b007ea
Step 12/12 : ENTRYPOINT [ "node", "index.js" ]
 ---> Running in b64a15932950
Removing intermediate container b64a15932950
 ---> f1800a4a650b
Successfully built f1800a4a650b
Successfully tagged mwanthi/paymentservice:latest
[Pipeline] sh
+ docker tag mwanthi/paymentservice mwanthi/paymentservice:v0.0.1
[Pipeline] sh
+ docker push mwanthi/paymentservice:v0.0.1
The push refers to repository [docker.io/mwanthi/paymentservice]
ad851967c408: Preparing
4e8d2e1e779d: Preparing
8710804fd7d3: Preparing
a1a4b7295e90: Preparing
63ca1fbb43ae: Preparing
63ca1fbb43ae: Mounted from mwanthi/currencyservice
ad851967c408: Pushed
8710804fd7d3: Pushed
a1a4b7295e90: Pushed
4e8d2e1e779d: Pushed
v0.0.1: digest: sha256:263f78b96345da1ac6c893bc79f46fddd3e624b98124463b6a222e1bd202e1ee size: 1368
[Pipeline] sh
+ docker push mwanthi/paymentservice:latest
The push refers to repository [docker.io/mwanthi/paymentservice]
ad851967c408: Preparing
4e8d2e1e779d: Preparing
8710804fd7d3: Preparing
a1a4b7295e90: Preparing
63ca1fbb43ae: Preparing
63ca1fbb43ae: Layer already exists
4e8d2e1e779d: Layer already exists
ad851967c408: Layer already exists
8710804fd7d3: Layer already exists
a1a4b7295e90: Layer already exists
latest: digest: sha256:263f78b96345da1ac6c893bc79f46fddd3e624b98124463b6a222e1bd202e1ee size: 1368
[Pipeline] sh
+ sed -i  -e s|mwanthi/paymentservice:v0.0.1|mwanthi/paymentservice:v0.0.1|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/paymentservice/paymentservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/paymentservice:latest
Untagged: mwanthi/paymentservice:latest
[Pipeline] sh
+ docker rmi mwanthi/paymentservice:v0.0.1
Untagged: mwanthi/paymentservice:v0.0.1
Untagged: mwanthi/paymentservice@sha256:263f78b96345da1ac6c893bc79f46fddd3e624b98124463b6a222e1bd202e1ee
Deleted: sha256:f1800a4a650b8ca868fee39c889c467963ca8a1563a0cc6983cb09029af89b03
Deleted: sha256:b39bf8b007ea3b4b7c2b47cfe4789d80487621aaf4adf67695906167c9bbbec2
Deleted: sha256:b7fbaa4ff65719af4348e4a3ebc7c4c93698724624429a8006def95a0a8fb660
Deleted: sha256:ac6e3f336bd15b80e0f5a90f81b994b4179be19e9e5474aa4c761fafdee8b229
Deleted: sha256:60df2b90423022051960ca41435f0c69c742d2655fd8db432a977cc13082ed27
Deleted: sha256:e11e304286fbee981d88a3be41c650ca30d1533809649f289ea43f1fe08252c5
Deleted: sha256:69d0bf79899399a634c369d420e9a9cd338051bfdf67dee1cc569e4f078e82b1
Deleted: sha256:9308176cb67e58b1ba82c9d36c63213807b3367391839bad6796d6af29665bef
Deleted: sha256:11a7a060232281d5a039e90b414ebce977c5acfc06e1be70df0392ca595ca6d9
Deleted: sha256:c55eb9b59ffa519a2a4834c52c48dc156f359c1a3c393df31d4f700464cd637f
[Pipeline] sh
+ docker image prune -f
Deleted Images:
untagged: alpine@sha256:beefdbd8a1da6d2915566fde36db9db0b524eb737fc57cd1367effd16dc0d06d
deleted: sha256:91ef0af61f39ece4d6710e465df5ed6ca12112358344fd51ae6a3b886634148b
untagged: python@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26
deleted: sha256:86b8b6de4ba2edaa00b6721a7d77a19dc0b20642af20f772b71152fda8d5a3a8
deleted: sha256:06cd4d7df090c22215821a922931f3b2063b7540b1a380407c764a102b128491
deleted: sha256:74a2d6d826bd4906ec5ea1b9b11e1a01f5d2053a86165d59badf7a3677741847
deleted: sha256:0e0d8c7ac030d9d8fad72239164c1f2fde61d0590c35a4c07c4a2f3aa027baaf
deleted: sha256:8d853c8add5d1e7b0aafc4b68a3d9fb8e7a0da27970c2acf831fe63be4a0cd2c
deleted: sha256:46cf021a968d99e4e065231a269808599c38843c35b089452e44ea77a0b1a292
deleted: sha256:30ae8bd986523c7a9341529b4d61cf5781c7a4180838f0f62e24b290d4a295a5
deleted: sha256:0bcaa9e0ebddd6e9aaaadbc88c664a5d8f037ca4ca98e96180f04c10e51c7859
deleted: sha256:57f0a5781f5a2f9d5f6fd3899b06ee5094fdf1dc6c11a91e73e2fb5e63d10628
deleted: sha256:667091fea171efcd9b7455d90c9e28abb3b8375c96115fa77a19707785b1116b
deleted: sha256:de9d97cf8e3b0825ce94faa6173ee0133fa1d1cb8042925f1153654b1d692bff
deleted: sha256:183db401887a51a9b08052a5db5073daf65d92dd9a7b699e859d9f1804ac3b05
deleted: sha256:9f3ef6e423fd6a1a94b96dc84bbc86850b9f66748e3bb47dd7ebd62eda58b1ec

Total reclaimed space: 520.8MB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] echo
Tracking and building productcatalogservice service...
[Pipeline] sh
+ echo productcatalogservice
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Building and Pushing productcatalogservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/3e80f504-e7eb-4882-adfd-aa96f76954cc/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ grep image: mwanthi/productcatalogservice:[^[:space:]]* /home/ubuntu/workspace/microservices-build/kubernetes-manifests/productcatalogservice/productcatalogservice.yaml
+ + awkawk {gsub(/^v/, ""); print} -F
 : {print $3}
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app/src/productcatalogservice
[Pipeline] {
[Pipeline] sh
+ docker build --no-cache -t mwanthi/productcatalogservice .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  203.3kB

Step 1/15 : FROM golang:1.23.1-alpine@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06 AS builder
docker.io/library/golang:1.23.1-alpine@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06: Pulling from library/golang
43c4264eed91: Already exists
ab19dfae90ef: Pulling fs layer
e7bff916ab0c: Pulling fs layer
78cee99375e3: Pulling fs layer
4f4fb700ef54: Pulling fs layer
4f4fb700ef54: Waiting
78cee99375e3: Download complete
ab19dfae90ef: Verifying Checksum
ab19dfae90ef: Download complete
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
Step 2/15 : WORKDIR /src
 ---> Running in 5f80b79de04a
Removing intermediate container 5f80b79de04a
 ---> df9069e48cf5
Step 3/15 : COPY go.mod go.sum ./
 ---> af9ee760170e
Step 4/15 : RUN go mod download
 ---> Running in b8260f3235ed
Removing intermediate container b8260f3235ed
 ---> 3a3d2853844a
Step 5/15 : COPY . .
 ---> c463174eb442
Step 6/15 : ARG SKAFFOLD_GO_GCFLAGS
 ---> Running in 0586f9b36d8e
Removing intermediate container 0586f9b36d8e
 ---> 5c2ff5800825
Step 7/15 : RUN CGO_ENABLED=0 GOOS=linux go build -gcflags="${SKAFFOLD_GO_GCFLAGS}" -o /productcatalogservice .
 ---> Running in e0f85c9e9476
Removing intermediate container e0f85c9e9476
 ---> 28e40cdebca9
Step 8/15 : FROM scratch
 ---> 
Step 9/15 : WORKDIR /src
 ---> Running in 9c7193977fd2
Removing intermediate container 9c7193977fd2
 ---> d16d4dde2c21
Step 10/15 : COPY --from=builder /productcatalogservice ./server
 ---> b65e64aec767
Step 11/15 : COPY --from=builder /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/ca-certificates.crt
 ---> 12ee7f3e5042
Step 12/15 : COPY products.json .
 ---> 7e155f549be1
Step 13/15 : ENV GOTRACEBACK=single
 ---> Running in 976bf5e65c0d
Removing intermediate container 976bf5e65c0d
 ---> 0b7ad197dac3
Step 14/15 : EXPOSE 3550
 ---> Running in c07d8bfd5324
Removing intermediate container c07d8bfd5324
 ---> 1ebf0059e89e
Step 15/15 : ENTRYPOINT ["/src/server"]
 ---> Running in 59a6231f290a
Removing intermediate container 59a6231f290a
 ---> 8c780b5eabcf
Successfully built 8c780b5eabcf
Successfully tagged mwanthi/productcatalogservice:latest
[Pipeline] sh
+ docker tag mwanthi/productcatalogservice mwanthi/productcatalogservice:v0.0.1
[Pipeline] sh
+ docker push mwanthi/productcatalogservice:v0.0.1
The push refers to repository [docker.io/mwanthi/productcatalogservice]
db18041cb08e: Preparing
20235bab2854: Preparing
221a2f2d5bbe: Preparing
6c2ce34bb3fb: Preparing
db18041cb08e: Pushed
6c2ce34bb3fb: Pushed
20235bab2854: Pushed
221a2f2d5bbe: Pushed
v0.0.1: digest: sha256:50509e649337a1fa312302c8ee23cf75d5ed1a30e348406144b71ab04c1706b7 size: 1152
[Pipeline] sh
+ docker push mwanthi/productcatalogservice:latest
The push refers to repository [docker.io/mwanthi/productcatalogservice]
db18041cb08e: Preparing
20235bab2854: Preparing
221a2f2d5bbe: Preparing
6c2ce34bb3fb: Preparing
db18041cb08e: Layer already exists
20235bab2854: Layer already exists
6c2ce34bb3fb: Layer already exists
221a2f2d5bbe: Layer already exists
latest: digest: sha256:50509e649337a1fa312302c8ee23cf75d5ed1a30e348406144b71ab04c1706b7 size: 1152
[Pipeline] sh
+ sed -i  -e s|mwanthi/productcatalogservice:v0.0.1|mwanthi/productcatalogservice:v0.0.1|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/productcatalogservice/productcatalogservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/productcatalogservice:latest
Untagged: mwanthi/productcatalogservice:latest
[Pipeline] sh
+ docker rmi mwanthi/productcatalogservice:v0.0.1
Untagged: mwanthi/productcatalogservice:v0.0.1
Untagged: mwanthi/productcatalogservice@sha256:50509e649337a1fa312302c8ee23cf75d5ed1a30e348406144b71ab04c1706b7
Deleted: sha256:8c780b5eabcf937038fc1593c24dcd8d45d2f7756e46ff12dcc64965a83718a0
Deleted: sha256:1ebf0059e89e83cca5eb7d6e318a13aaffc815ec6cda546426b50fab68934210
Deleted: sha256:0b7ad197dac31cb70e7bdc8bf77a402a3b1de06bd1bb965055139e93915b1036
Deleted: sha256:7e155f549be1c1ee1ce40a837ebb3df16be7b2a06d24265693c1513588603577
Deleted: sha256:2465fdd54142020ef5dd4547b5a8393e0fa99b8e3ffb37be3ccda2b1e1fd4db0
Deleted: sha256:12ee7f3e50422111792aee159ae35a7478c462dc3cd91346cf65981a3010326e
Deleted: sha256:0368d09eeedc3ab6d919f33caed590afccc13c84bcb6808dd82378513f0d4eef
Deleted: sha256:b65e64aec76710ac88c5665759a7545d29ffc5c8da0e1a312a8f444933c99d1a
Deleted: sha256:8d6800c3091fcb52f583e8c4c9ec436d30a56e991c92b21b3fc320c726d825a9
Deleted: sha256:d16d4dde2c213af31f65715faa1aa9d8de2e664db613b757ee8c031b5091ed59
Deleted: sha256:6c2ce34bb3fb90298578381c6fe16238a9376d31468ce05fda067ed0543ff0b2
[Pipeline] sh
+ docker image prune -f
Deleted Images:
deleted: sha256:28e40cdebca97ddc71d95222121dca2e3e4b79bf09fd53db2ca940b623e6605e
deleted: sha256:3a7d12c3b3bf0b04da3dd7165d21bc62c317a6c0a7b420cebccdbd5ef3c412fe
deleted: sha256:5c2ff58008255548d2b49254c0b30523a7c287014fa62e0cbbbb8a58dc55c501
deleted: sha256:c463174eb442e8b13188f601814e2f53b40e869e72626668e256882efa7db412
deleted: sha256:8b1ebbaccc3eb8226b1d8573e18c439b7602d6f36d7a17888acfb9b99396ba68
deleted: sha256:3a3d2853844a030e26ab01ea11763bb5fa1143d538fb9c70ba481665bc15a125
deleted: sha256:436309d54b3d8096d3af721102f656882199a02a519ee531e1fac60229354637
deleted: sha256:af9ee760170eaa36c5e1d9cd77ce89dbc90e7e6ccf7b3d7e3900148ef0defa16
deleted: sha256:8e210909ba6a83aeaed4512cb3e58d1093cff8da1ff52763a331e1585043622b
deleted: sha256:df9069e48cf5b0cc71a884d38267a0504b0621427f23f06ca1f4231c815291a0
deleted: sha256:73faeb6ad4a07c5d9ef7b2c061406d25bad46c1b3b5783f4918e16ac875837f1
untagged: node@sha256:2d07db07a2df6830718ae2a47db6fedce6745f5bcd174c398f2acdda90a11c03
deleted: sha256:45a59611ca84e7fa7e39413f7a657afd43e2b71b8d6cb3cb722d97ffc842decb
deleted: sha256:5224d953fb6159064b9b661e6ea7dda03b4b8ab8eceea889cddb0681220b5322
deleted: sha256:066954302d87006fb52541c44830d87caed51a4d3f60227077cf035619255889
deleted: sha256:9561d1ac6ce7491afee33934a225d0b100cdc011fcd45274b98425090dae4bac

Total reclaimed space: 957.7MB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] echo
Tracking and building recommendationservice service...
[Pipeline] sh
+ echo recommendationservice
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Building and Pushing recommendationservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/45586c8a-85e1-4a36-b456-0b4bfa0e1101/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ + awkgrep {gsub(/^v/, ""); print} image: mwanthi/recommendationservice:[^[:space:]]*
 /home/ubuntu/workspace/microservices-build/kubernetes-manifests/recommendationservice/recommendationservice.yaml
+ awk -F : {print $3}
[Pipeline] dir
Running in /home/ubuntu/workspace/microservices-build/microservices-app/src/recommendationservice
[Pipeline] {
[Pipeline] sh
+ docker build --no-cache -t mwanthi/recommendationservice .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  62.98kB

Step 1/13 : FROM python:3.12.6-slim@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26 AS base
docker.io/library/python:3.12.6-slim@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26: Pulling from library/python
302e3ee49805: Pulling fs layer
699edf835b1b: Pulling fs layer
417a872b7725: Pulling fs layer
9795987f6d21: Pulling fs layer
9795987f6d21: Waiting
699edf835b1b: Verifying Checksum
699edf835b1b: Download complete
417a872b7725: Verifying Checksum
417a872b7725: Download complete
302e3ee49805: Verifying Checksum
302e3ee49805: Download complete
9795987f6d21: Verifying Checksum
9795987f6d21: Download complete
302e3ee49805: Pull complete
699edf835b1b: Pull complete
417a872b7725: Pull complete
9795987f6d21: Pull complete
Digest: sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26
Status: Downloaded newer image for python:3.12.6-slim@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26
 ---> 86b8b6de4ba2
Step 2/13 : FROM base AS builder
 ---> 86b8b6de4ba2
Step 3/13 : RUN apt-get -qq update     && apt-get install -y --no-install-recommends         wget g++     && rm -rf /var/lib/apt/lists/*
 ---> Running in 525d86cd8905
Reading package lists...
Building dependency tree...
Reading state information...
The following additional packages will be installed:
  binutils binutils-common binutils-x86-64-linux-gnu cpp cpp-12 g++-12 gcc
  gcc-12 libasan8 libatomic1 libbinutils libc-dev-bin libc6-dev libcc1-0
  libcrypt-dev libctf-nobfd0 libctf0 libgcc-12-dev libgomp1 libgprofng0
  libisl23 libitm1 libjansson4 liblsan0 libmpc3 libmpfr6 libnsl-dev libpsl5
  libquadmath0 libstdc++-12-dev libtirpc-dev libtsan2 libubsan1 linux-libc-dev
  rpcsvc-proto
Suggested packages:
  binutils-doc cpp-doc gcc-12-locales cpp-12-doc g++-multilib g++-12-multilib
  gcc-12-doc gcc-multilib make manpages-dev autoconf automake libtool flex
  bison gdb gcc-doc gcc-12-multilib glibc-doc libstdc++-12-doc
Recommended packages:
  manpages manpages-dev libc-devtools publicsuffix
The following NEW packages will be installed:
  binutils binutils-common binutils-x86-64-linux-gnu cpp cpp-12 g++ g++-12 gcc
  gcc-12 libasan8 libatomic1 libbinutils libc-dev-bin libc6-dev libcc1-0
  libcrypt-dev libctf-nobfd0 libctf0 libgcc-12-dev libgomp1 libgprofng0
  libisl23 libitm1 libjansson4 liblsan0 libmpc3 libmpfr6 libnsl-dev libpsl5
  libquadmath0 libstdc++-12-dev libtirpc-dev libtsan2 libubsan1 linux-libc-dev
  rpcsvc-proto wget
0 upgraded, 37 newly installed, 0 to remove and 0 not upgraded.
Need to get 64.2 MB of archives.
After this operation, 262 MB of additional disk space will be used.
Get:1 http://deb.debian.org/debian bookworm/main amd64 libpsl5 amd64 0.21.2-1 [58.7 kB]
Get:2 http://deb.debian.org/debian bookworm/main amd64 wget amd64 1.21.3-1+b2 [984 kB]
Get:3 http://deb.debian.org/debian bookworm/main amd64 binutils-common amd64 2.40-2 [2487 kB]
Get:4 http://deb.debian.org/debian bookworm/main amd64 libbinutils amd64 2.40-2 [572 kB]
Get:5 http://deb.debian.org/debian bookworm/main amd64 libctf-nobfd0 amd64 2.40-2 [153 kB]
Get:6 http://deb.debian.org/debian bookworm/main amd64 libctf0 amd64 2.40-2 [89.8 kB]
Get:7 http://deb.debian.org/debian bookworm/main amd64 libgprofng0 amd64 2.40-2 [812 kB]
Get:8 http://deb.debian.org/debian bookworm/main amd64 libjansson4 amd64 2.14-2 [40.8 kB]
Get:9 http://deb.debian.org/debian bookworm/main amd64 binutils-x86-64-linux-gnu amd64 2.40-2 [2246 kB]
Get:10 http://deb.debian.org/debian bookworm/main amd64 binutils amd64 2.40-2 [65.0 kB]
Get:11 http://deb.debian.org/debian bookworm/main amd64 libisl23 amd64 0.25-1.1 [683 kB]
Get:12 http://deb.debian.org/debian bookworm/main amd64 libmpfr6 amd64 4.2.0-1 [701 kB]
Get:13 http://deb.debian.org/debian bookworm/main amd64 libmpc3 amd64 1.3.1-1 [51.5 kB]
Get:14 http://deb.debian.org/debian bookworm/main amd64 cpp-12 amd64 12.2.0-14 [9764 kB]
Get:15 http://deb.debian.org/debian bookworm/main amd64 cpp amd64 4:12.2.0-3 [6836 B]
Get:16 http://deb.debian.org/debian bookworm/main amd64 libcc1-0 amd64 12.2.0-14 [41.7 kB]
Get:17 http://deb.debian.org/debian bookworm/main amd64 libgomp1 amd64 12.2.0-14 [116 kB]
Get:18 http://deb.debian.org/debian bookworm/main amd64 libitm1 amd64 12.2.0-14 [26.1 kB]
Get:19 http://deb.debian.org/debian bookworm/main amd64 libatomic1 amd64 12.2.0-14 [9328 B]
Get:20 http://deb.debian.org/debian bookworm/main amd64 libasan8 amd64 12.2.0-14 [2195 kB]
Get:21 http://deb.debian.org/debian bookworm/main amd64 liblsan0 amd64 12.2.0-14 [969 kB]
Get:22 http://deb.debian.org/debian bookworm/main amd64 libtsan2 amd64 12.2.0-14 [2196 kB]
Get:23 http://deb.debian.org/debian bookworm/main amd64 libubsan1 amd64 12.2.0-14 [883 kB]
Get:24 http://deb.debian.org/debian bookworm/main amd64 libquadmath0 amd64 12.2.0-14 [144 kB]
Get:25 http://deb.debian.org/debian bookworm/main amd64 libgcc-12-dev amd64 12.2.0-14 [2437 kB]
Get:26 http://deb.debian.org/debian bookworm/main amd64 gcc-12 amd64 12.2.0-14 [19.3 MB]
Get:27 http://deb.debian.org/debian bookworm/main amd64 gcc amd64 4:12.2.0-3 [5216 B]
Get:28 http://deb.debian.org/debian bookworm/main amd64 libc-dev-bin amd64 2.36-9+deb12u8 [46.3 kB]
Get:29 http://deb.debian.org/debian-security bookworm-security/main amd64 linux-libc-dev amd64 6.1.112-1 [2043 kB]
Get:30 http://deb.debian.org/debian bookworm/main amd64 libcrypt-dev amd64 1:4.4.33-2 [118 kB]
Get:31 http://deb.debian.org/debian bookworm/main amd64 libtirpc-dev amd64 1.3.3+ds-1 [191 kB]
Get:32 http://deb.debian.org/debian bookworm/main amd64 libnsl-dev amd64 1.3.0-2 [66.4 kB]
Get:33 http://deb.debian.org/debian bookworm/main amd64 rpcsvc-proto amd64 1.4.3-1 [63.3 kB]
Get:34 http://deb.debian.org/debian bookworm/main amd64 libc6-dev amd64 2.36-9+deb12u8 [1900 kB]
Get:35 http://deb.debian.org/debian bookworm/main amd64 libstdc++-12-dev amd64 12.2.0-14 [2046 kB]
Get:36 http://deb.debian.org/debian bookworm/main amd64 g++-12 amd64 12.2.0-14 [10.7 MB]
Get:37 http://deb.debian.org/debian bookworm/main amd64 g++ amd64 4:12.2.0-3 [1356 B]
[91mdebconf: delaying package configuration, since apt-utils is not installed
[0mFetched 64.2 MB in 1s (89.8 MB/s)
Selecting previously unselected package libpsl5:amd64.
(Reading database ... 
(Reading database ... 5%
(Reading database ... 10%
(Reading database ... 15%
(Reading database ... 20%
(Reading database ... 25%
(Reading database ... 30%
(Reading database ... 35%
(Reading database ... 40%
(Reading database ... 45%
(Reading database ... 50%
(Reading database ... 55%
(Reading database ... 60%
(Reading database ... 65%
(Reading database ... 70%
(Reading database ... 75%
(Reading database ... 80%
(Reading database ... 85%
(Reading database ... 90%
(Reading database ... 95%
(Reading database ... 100%
(Reading database ... 6695 files and directories currently installed.)
Preparing to unpack .../00-libpsl5_0.21.2-1_amd64.deb ...
Unpacking libpsl5:amd64 (0.21.2-1) ...
Selecting previously unselected package wget.
Preparing to unpack .../01-wget_1.21.3-1+b2_amd64.deb ...
Unpacking wget (1.21.3-1+b2) ...
Selecting previously unselected package binutils-common:amd64.
Preparing to unpack .../02-binutils-common_2.40-2_amd64.deb ...
Unpacking binutils-common:amd64 (2.40-2) ...
Selecting previously unselected package libbinutils:amd64.
Preparing to unpack .../03-libbinutils_2.40-2_amd64.deb ...
Unpacking libbinutils:amd64 (2.40-2) ...
Selecting previously unselected package libctf-nobfd0:amd64.
Preparing to unpack .../04-libctf-nobfd0_2.40-2_amd64.deb ...
Unpacking libctf-nobfd0:amd64 (2.40-2) ...
Selecting previously unselected package libctf0:amd64.
Preparing to unpack .../05-libctf0_2.40-2_amd64.deb ...
Unpacking libctf0:amd64 (2.40-2) ...
Selecting previously unselected package libgprofng0:amd64.
Preparing to unpack .../06-libgprofng0_2.40-2_amd64.deb ...
Unpacking libgprofng0:amd64 (2.40-2) ...
Selecting previously unselected package libjansson4:amd64.
Preparing to unpack .../07-libjansson4_2.14-2_amd64.deb ...
Unpacking libjansson4:amd64 (2.14-2) ...
Selecting previously unselected package binutils-x86-64-linux-gnu.
Preparing to unpack .../08-binutils-x86-64-linux-gnu_2.40-2_amd64.deb ...
Unpacking binutils-x86-64-linux-gnu (2.40-2) ...
Selecting previously unselected package binutils.
Preparing to unpack .../09-binutils_2.40-2_amd64.deb ...
Unpacking binutils (2.40-2) ...
Selecting previously unselected package libisl23:amd64.
Preparing to unpack .../10-libisl23_0.25-1.1_amd64.deb ...
Unpacking libisl23:amd64 (0.25-1.1) ...
Selecting previously unselected package libmpfr6:amd64.
Preparing to unpack .../11-libmpfr6_4.2.0-1_amd64.deb ...
Unpacking libmpfr6:amd64 (4.2.0-1) ...
Selecting previously unselected package libmpc3:amd64.
Preparing to unpack .../12-libmpc3_1.3.1-1_amd64.deb ...
Unpacking libmpc3:amd64 (1.3.1-1) ...
Selecting previously unselected package cpp-12.
Preparing to unpack .../13-cpp-12_12.2.0-14_amd64.deb ...
Unpacking cpp-12 (12.2.0-14) ...
Selecting previously unselected package cpp.
Preparing to unpack .../14-cpp_4%3a12.2.0-3_amd64.deb ...
Unpacking cpp (4:12.2.0-3) ...
Selecting previously unselected package libcc1-0:amd64.
Preparing to unpack .../15-libcc1-0_12.2.0-14_amd64.deb ...
Unpacking libcc1-0:amd64 (12.2.0-14) ...
Selecting previously unselected package libgomp1:amd64.
Preparing to unpack .../16-libgomp1_12.2.0-14_amd64.deb ...
Unpacking libgomp1:amd64 (12.2.0-14) ...
Selecting previously unselected package libitm1:amd64.
Preparing to unpack .../17-libitm1_12.2.0-14_amd64.deb ...
Unpacking libitm1:amd64 (12.2.0-14) ...
Selecting previously unselected package libatomic1:amd64.
Preparing to unpack .../18-libatomic1_12.2.0-14_amd64.deb ...
Unpacking libatomic1:amd64 (12.2.0-14) ...
Selecting previously unselected package libasan8:amd64.
Preparing to unpack .../19-libasan8_12.2.0-14_amd64.deb ...
Unpacking libasan8:amd64 (12.2.0-14) ...
Selecting previously unselected package liblsan0:amd64.
Preparing to unpack .../20-liblsan0_12.2.0-14_amd64.deb ...
Unpacking liblsan0:amd64 (12.2.0-14) ...
Selecting previously unselected package libtsan2:amd64.
Preparing to unpack .../21-libtsan2_12.2.0-14_amd64.deb ...
Unpacking libtsan2:amd64 (12.2.0-14) ...
Selecting previously unselected package libubsan1:amd64.
Preparing to unpack .../22-libubsan1_12.2.0-14_amd64.deb ...
Unpacking libubsan1:amd64 (12.2.0-14) ...
Selecting previously unselected package libquadmath0:amd64.
Preparing to unpack .../23-libquadmath0_12.2.0-14_amd64.deb ...
Unpacking libquadmath0:amd64 (12.2.0-14) ...
Selecting previously unselected package libgcc-12-dev:amd64.
Preparing to unpack .../24-libgcc-12-dev_12.2.0-14_amd64.deb ...
Unpacking libgcc-12-dev:amd64 (12.2.0-14) ...
Selecting previously unselected package gcc-12.
Preparing to unpack .../25-gcc-12_12.2.0-14_amd64.deb ...
Unpacking gcc-12 (12.2.0-14) ...
Selecting previously unselected package gcc.
Preparing to unpack .../26-gcc_4%3a12.2.0-3_amd64.deb ...
Unpacking gcc (4:12.2.0-3) ...
Selecting previously unselected package libc-dev-bin.
Preparing to unpack .../27-libc-dev-bin_2.36-9+deb12u8_amd64.deb ...
Unpacking libc-dev-bin (2.36-9+deb12u8) ...
Selecting previously unselected package linux-libc-dev:amd64.
Preparing to unpack .../28-linux-libc-dev_6.1.112-1_amd64.deb ...
Unpacking linux-libc-dev:amd64 (6.1.112-1) ...
Selecting previously unselected package libcrypt-dev:amd64.
Preparing to unpack .../29-libcrypt-dev_1%3a4.4.33-2_amd64.deb ...
Unpacking libcrypt-dev:amd64 (1:4.4.33-2) ...
Selecting previously unselected package libtirpc-dev:amd64.
Preparing to unpack .../30-libtirpc-dev_1.3.3+ds-1_amd64.deb ...
Unpacking libtirpc-dev:amd64 (1.3.3+ds-1) ...
Selecting previously unselected package libnsl-dev:amd64.
Preparing to unpack .../31-libnsl-dev_1.3.0-2_amd64.deb ...
Unpacking libnsl-dev:amd64 (1.3.0-2) ...
Selecting previously unselected package rpcsvc-proto.
Preparing to unpack .../32-rpcsvc-proto_1.4.3-1_amd64.deb ...
Unpacking rpcsvc-proto (1.4.3-1) ...
Selecting previously unselected package libc6-dev:amd64.
Preparing to unpack .../33-libc6-dev_2.36-9+deb12u8_amd64.deb ...
Unpacking libc6-dev:amd64 (2.36-9+deb12u8) ...
Selecting previously unselected package libstdc++-12-dev:amd64.
Preparing to unpack .../34-libstdc++-12-dev_12.2.0-14_amd64.deb ...
Unpacking libstdc++-12-dev:amd64 (12.2.0-14) ...
Selecting previously unselected package g++-12.
Preparing to unpack .../35-g++-12_12.2.0-14_amd64.deb ...
Unpacking g++-12 (12.2.0-14) ...
Selecting previously unselected package g++.
Preparing to unpack .../36-g++_4%3a12.2.0-3_amd64.deb ...
Unpacking g++ (4:12.2.0-3) ...
Setting up libpsl5:amd64 (0.21.2-1) ...
Setting up wget (1.21.3-1+b2) ...
Setting up binutils-common:amd64 (2.40-2) ...
Setting up linux-libc-dev:amd64 (6.1.112-1) ...
Setting up libctf-nobfd0:amd64 (2.40-2) ...
Setting up libgomp1:amd64 (12.2.0-14) ...
Setting up libjansson4:amd64 (2.14-2) ...
Setting up libtirpc-dev:amd64 (1.3.3+ds-1) ...
Setting up rpcsvc-proto (1.4.3-1) ...
Setting up libmpfr6:amd64 (4.2.0-1) ...
Setting up libquadmath0:amd64 (12.2.0-14) ...
Setting up libmpc3:amd64 (1.3.1-1) ...
Setting up libatomic1:amd64 (12.2.0-14) ...
Setting up libubsan1:amd64 (12.2.0-14) ...
Setting up libnsl-dev:amd64 (1.3.0-2) ...
Setting up libcrypt-dev:amd64 (1:4.4.33-2) ...
Setting up libasan8:amd64 (12.2.0-14) ...
Setting up libtsan2:amd64 (12.2.0-14) ...
Setting up libbinutils:amd64 (2.40-2) ...
Setting up libisl23:amd64 (0.25-1.1) ...
Setting up libc-dev-bin (2.36-9+deb12u8) ...
Setting up libcc1-0:amd64 (12.2.0-14) ...
Setting up liblsan0:amd64 (12.2.0-14) ...
Setting up libitm1:amd64 (12.2.0-14) ...
Setting up libctf0:amd64 (2.40-2) ...
Setting up cpp-12 (12.2.0-14) ...
Setting up libgprofng0:amd64 (2.40-2) ...
Setting up libgcc-12-dev:amd64 (12.2.0-14) ...
Setting up cpp (4:12.2.0-3) ...
Setting up libc6-dev:amd64 (2.36-9+deb12u8) ...
Setting up binutils-x86-64-linux-gnu (2.40-2) ...
Setting up libstdc++-12-dev:amd64 (12.2.0-14) ...
Setting up binutils (2.40-2) ...
Setting up gcc-12 (12.2.0-14) ...
Setting up g++-12 (12.2.0-14) ...
Setting up gcc (4:12.2.0-3) ...
Setting up g++ (4:12.2.0-3) ...
update-alternatives: using /usr/bin/g++ to provide /usr/bin/c++ (c++) in auto mode
Processing triggers for libc-bin (2.36-9+deb12u8) ...
Removing intermediate container 525d86cd8905
 ---> 80b3f931c8df
Step 4/13 : COPY requirements.txt .
 ---> 243796190c0b
Step 5/13 : RUN pip install -r requirements.txt
 ---> Running in b4915c7c7452
Collecting backoff==2.2.1 (from -r requirements.txt (line 7))
  Downloading backoff-2.2.1-py3-none-any.whl.metadata (14 kB)
Collecting cachetools==5.3.2 (from -r requirements.txt (line 11))
  Downloading cachetools-5.3.2-py3-none-any.whl.metadata (5.2 kB)
Collecting certifi==2023.7.22 (from -r requirements.txt (line 13))
  Downloading certifi-2023.7.22-py3-none-any.whl.metadata (2.2 kB)
Collecting charset-normalizer==3.3.2 (from -r requirements.txt (line 15))
  Downloading charset_normalizer-3.3.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (33 kB)
Collecting deprecated==1.2.14 (from -r requirements.txt (line 17))
  Downloading Deprecated-1.2.14-py2.py3-none-any.whl.metadata (5.4 kB)
Collecting google-api-core==2.12.0 (from -r requirements.txt (line 21))
  Downloading google_api_core-2.12.0-py3-none-any.whl.metadata (2.7 kB)
Collecting google-api-python-client==2.107.0 (from -r requirements.txt (line 25))
  Downloading google_api_python_client-2.107.0-py2.py3-none-any.whl.metadata (6.6 kB)
Collecting google-auth==2.23.4 (from -r requirements.txt (line 27))
  Downloading google_auth-2.23.4-py2.py3-none-any.whl.metadata (4.7 kB)
Collecting google-auth-httplib2==0.1.1 (from -r requirements.txt (line 33))
  Downloading google_auth_httplib2-0.1.1-py2.py3-none-any.whl.metadata (2.1 kB)
Collecting google-cloud-profiler==4.1.0 (from -r requirements.txt (line 37))
  Downloading google-cloud-profiler-4.1.0.tar.gz (32 kB)
  Installing build dependencies: started
  Installing build dependencies: finished with status 'done'
  Getting requirements to build wheel: started
  Getting requirements to build wheel: finished with status 'done'
  Installing backend dependencies: started
  Installing backend dependencies: finished with status 'done'
  Preparing metadata (pyproject.toml): started
  Preparing metadata (pyproject.toml): finished with status 'done'
Collecting googleapis-common-protos==1.61.0 (from -r requirements.txt (line 39))
  Downloading googleapis_common_protos-1.61.0-py2.py3-none-any.whl.metadata (1.5 kB)
Collecting grpcio==1.59.2 (from -r requirements.txt (line 43))
  Downloading grpcio-1.59.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (4.0 kB)
Collecting grpcio-health-checking==1.59.2 (from -r requirements.txt (line 47))
  Downloading grpcio_health_checking-1.59.2-py3-none-any.whl.metadata (1.3 kB)
Collecting httplib2==0.22.0 (from -r requirements.txt (line 49))
  Downloading httplib2-0.22.0-py3-none-any.whl.metadata (2.6 kB)
Collecting idna==3.4 (from -r requirements.txt (line 53))
  Downloading idna-3.4-py3-none-any.whl.metadata (9.8 kB)
Collecting importlib-metadata==6.8.0 (from -r requirements.txt (line 55))
  Downloading importlib_metadata-6.8.0-py3-none-any.whl.metadata (5.1 kB)
Collecting opentelemetry-api==1.20.0 (from -r requirements.txt (line 57))
  Downloading opentelemetry_api-1.20.0-py3-none-any.whl.metadata (1.4 kB)
Collecting opentelemetry-distro==0.41b0 (from -r requirements.txt (line 64))
  Downloading opentelemetry_distro-0.41b0-py3-none-any.whl.metadata (1.5 kB)
Collecting opentelemetry-exporter-otlp-proto-common==1.20.0 (from -r requirements.txt (line 66))
  Downloading opentelemetry_exporter_otlp_proto_common-1.20.0-py3-none-any.whl.metadata (1.8 kB)
Collecting opentelemetry-exporter-otlp-proto-grpc==1.20.0 (from -r requirements.txt (line 68))
  Downloading opentelemetry_exporter_otlp_proto_grpc-1.20.0-py3-none-any.whl.metadata (2.4 kB)
Collecting opentelemetry-instrumentation==0.41b0 (from -r requirements.txt (line 70))
  Downloading opentelemetry_instrumentation-0.41b0-py3-none-any.whl.metadata (5.9 kB)
Collecting opentelemetry-instrumentation-grpc==0.41b0 (from -r requirements.txt (line 74))
  Downloading opentelemetry_instrumentation_grpc-0.41b0-py3-none-any.whl.metadata (2.2 kB)
Collecting opentelemetry-proto==1.20.0 (from -r requirements.txt (line 76))
  Downloading opentelemetry_proto-1.20.0-py3-none-any.whl.metadata (2.3 kB)
Collecting opentelemetry-sdk==1.20.0 (from -r requirements.txt (line 80))
  Downloading opentelemetry_sdk-1.20.0-py3-none-any.whl.metadata (1.5 kB)
Collecting opentelemetry-semantic-conventions==0.41b0 (from -r requirements.txt (line 85))
  Downloading opentelemetry_semantic_conventions-0.41b0-py3-none-any.whl.metadata (2.3 kB)
Collecting protobuf==4.25.0 (from -r requirements.txt (line 89))
  Downloading protobuf-4.25.0-cp37-abi3-manylinux2014_x86_64.whl.metadata (541 bytes)
Collecting pyasn1==0.5.0 (from -r requirements.txt (line 96))
  Downloading pyasn1-0.5.0-py2.py3-none-any.whl.metadata (8.5 kB)
Collecting pyasn1-modules==0.3.0 (from -r requirements.txt (line 100))
  Downloading pyasn1_modules-0.3.0-py2.py3-none-any.whl.metadata (3.6 kB)
Collecting pyparsing==3.1.1 (from -r requirements.txt (line 102))
  Downloading pyparsing-3.1.1-py3-none-any.whl.metadata (5.1 kB)
Collecting python-json-logger==2.0.7 (from -r requirements.txt (line 104))
  Downloading python_json_logger-2.0.7-py3-none-any.whl.metadata (6.5 kB)
Collecting requests==2.31.0 (from -r requirements.txt (line 106))
  Downloading requests-2.31.0-py3-none-any.whl.metadata (4.6 kB)
Collecting rsa==4.9 (from -r requirements.txt (line 111))
  Downloading rsa-4.9-py3-none-any.whl.metadata (4.2 kB)
Collecting typing-extensions==4.8.0 (from -r requirements.txt (line 115))
  Downloading typing_extensions-4.8.0-py3-none-any.whl.metadata (3.0 kB)
Collecting uritemplate==4.1.1 (from -r requirements.txt (line 117))
  Downloading uritemplate-4.1.1-py2.py3-none-any.whl.metadata (2.9 kB)
Collecting urllib3==2.0.7 (from -r requirements.txt (line 119))
  Downloading urllib3-2.0.7-py3-none-any.whl.metadata (6.6 kB)
Collecting wrapt==1.16.0 (from -r requirements.txt (line 121))
  Downloading wrapt-1.16.0-cp312-cp312-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (6.6 kB)
Collecting zipp==3.17.0 (from -r requirements.txt (line 126))
  Downloading zipp-3.17.0-py3-none-any.whl.metadata (3.7 kB)
Collecting setuptools>=16.0 (from opentelemetry-instrumentation==0.41b0->-r requirements.txt (line 70))
  Using cached setuptools-75.3.0-py3-none-any.whl.metadata (6.9 kB)
Downloading backoff-2.2.1-py3-none-any.whl (15 kB)
Downloading cachetools-5.3.2-py3-none-any.whl (9.3 kB)
Downloading certifi-2023.7.22-py3-none-any.whl (158 kB)
Downloading charset_normalizer-3.3.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (141 kB)
Downloading Deprecated-1.2.14-py2.py3-none-any.whl (9.6 kB)
Downloading google_api_core-2.12.0-py3-none-any.whl (121 kB)
Downloading google_api_python_client-2.107.0-py2.py3-none-any.whl (12.7 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 12.7/12.7 MB 64.6 MB/s eta 0:00:00
Downloading google_auth-2.23.4-py2.py3-none-any.whl (183 kB)
Downloading google_auth_httplib2-0.1.1-py2.py3-none-any.whl (9.3 kB)
Downloading googleapis_common_protos-1.61.0-py2.py3-none-any.whl (230 kB)
Downloading grpcio-1.59.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (5.2 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 5.2/5.2 MB 98.7 MB/s eta 0:00:00
Downloading grpcio_health_checking-1.59.2-py3-none-any.whl (17 kB)
Downloading httplib2-0.22.0-py3-none-any.whl (96 kB)
Downloading idna-3.4-py3-none-any.whl (61 kB)
Downloading importlib_metadata-6.8.0-py3-none-any.whl (22 kB)
Downloading opentelemetry_api-1.20.0-py3-none-any.whl (57 kB)
Downloading opentelemetry_distro-0.41b0-py3-none-any.whl (3.3 kB)
Downloading opentelemetry_exporter_otlp_proto_common-1.20.0-py3-none-any.whl (17 kB)
Downloading opentelemetry_exporter_otlp_proto_grpc-1.20.0-py3-none-any.whl (18 kB)
Downloading opentelemetry_instrumentation-0.41b0-py3-none-any.whl (25 kB)
Downloading opentelemetry_instrumentation_grpc-0.41b0-py3-none-any.whl (26 kB)
Downloading opentelemetry_proto-1.20.0-py3-none-any.whl (50 kB)
Downloading opentelemetry_sdk-1.20.0-py3-none-any.whl (103 kB)
Downloading opentelemetry_semantic_conventions-0.41b0-py3-none-any.whl (26 kB)
Downloading protobuf-4.25.0-cp37-abi3-manylinux2014_x86_64.whl (294 kB)
Downloading pyasn1-0.5.0-py2.py3-none-any.whl (83 kB)
Downloading pyasn1_modules-0.3.0-py2.py3-none-any.whl (181 kB)
Downloading pyparsing-3.1.1-py3-none-any.whl (103 kB)
Downloading python_json_logger-2.0.7-py3-none-any.whl (8.1 kB)
Downloading requests-2.31.0-py3-none-any.whl (62 kB)
Downloading rsa-4.9-py3-none-any.whl (34 kB)
Downloading typing_extensions-4.8.0-py3-none-any.whl (31 kB)
Downloading uritemplate-4.1.1-py2.py3-none-any.whl (10 kB)
Downloading urllib3-2.0.7-py3-none-any.whl (124 kB)
Downloading wrapt-1.16.0-cp312-cp312-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (87 kB)
Downloading zipp-3.17.0-py3-none-any.whl (7.4 kB)
Using cached setuptools-75.3.0-py3-none-any.whl (1.3 MB)
Building wheels for collected packages: google-cloud-profiler
  Building wheel for google-cloud-profiler (pyproject.toml): started
  Building wheel for google-cloud-profiler (pyproject.toml): finished with status 'done'
  Created wheel for google-cloud-profiler: filename=google_cloud_profiler-4.1.0-cp312-cp312-linux_x86_64.whl size=761057 sha256=3b53befb1edd1ee1fb9a018e6b97592e419ce06a585784a59bb68c25895027c0
  Stored in directory: /root/.cache/pip/wheels/4c/e9/0e/051a26de1731259c679b0d9546e4a069b9e2adf536bb0566a2
Successfully built google-cloud-profiler
Installing collected packages: zipp, wrapt, urllib3, uritemplate, typing-extensions, setuptools, python-json-logger, pyparsing, pyasn1, protobuf, opentelemetry-semantic-conventions, idna, grpcio, charset-normalizer, certifi, cachetools, backoff, rsa, requests, pyasn1-modules, opentelemetry-proto, importlib-metadata, httplib2, grpcio-health-checking, googleapis-common-protos, deprecated, opentelemetry-exporter-otlp-proto-common, opentelemetry-api, google-auth, opentelemetry-sdk, opentelemetry-instrumentation, google-auth-httplib2, google-api-core, opentelemetry-instrumentation-grpc, opentelemetry-exporter-otlp-proto-grpc, opentelemetry-distro, google-api-python-client, google-cloud-profiler
Successfully installed backoff-2.2.1 cachetools-5.3.2 certifi-2023.7.22 charset-normalizer-3.3.2 deprecated-1.2.14 google-api-core-2.12.0 google-api-python-client-2.107.0 google-auth-2.23.4 google-auth-httplib2-0.1.1 google-cloud-profiler-4.1.0 googleapis-common-protos-1.61.0 grpcio-1.59.2 grpcio-health-checking-1.59.2 httplib2-0.22.0 idna-3.4 importlib-metadata-6.8.0 opentelemetry-api-1.20.0 opentelemetry-distro-0.41b0 opentelemetry-exporter-otlp-proto-common-1.20.0 opentelemetry-exporter-otlp-proto-grpc-1.20.0 opentelemetry-instrumentation-0.41b0 opentelemetry-instrumentation-grpc-0.41b0 opentelemetry-proto-1.20.0 opentelemetry-sdk-1.20.0 opentelemetry-semantic-conventions-0.41b0 protobuf-4.25.0 pyasn1-0.5.0 pyasn1-modules-0.3.0 pyparsing-3.1.1 python-json-logger-2.0.7 requests-2.31.0 rsa-4.9 setuptools-75.3.0 typing-extensions-4.8.0 uritemplate-4.1.1 urllib3-2.0.7 wrapt-1.16.0 zipp-3.17.0
[91mWARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager, possibly rendering your system unusable.It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv. Use the --root-user-action option if you know what you are doing and want to suppress this warning.
[0m[91m
[notice] A new release of pip is available: 24.2 -> 24.3.1
[notice] To update, run: pip install --upgrade pip
[0mRemoving intermediate container b4915c7c7452
 ---> e2e469875770
Step 6/13 : FROM base
 ---> 86b8b6de4ba2
Step 7/13 : ENV PYTHONUNBUFFERED=1
 ---> Running in 5f31fe851755
Removing intermediate container 5f31fe851755
 ---> cc21335e30fe
Step 8/13 : WORKDIR /recommendationservice
 ---> Running in 825858cdebcb
Removing intermediate container 825858cdebcb
 ---> e1e12f824c6a
Step 9/13 : COPY --from=builder /usr/local/lib/python3.12/ /usr/local/lib/python3.12/
 ---> 1e673499e116
Step 10/13 : COPY . .
 ---> 9ed270b19a83
Step 11/13 : ENV PORT "8080"
 ---> Running in 2e7c06511c3a
Removing intermediate container 2e7c06511c3a
 ---> fa6f2c6c809a
Step 12/13 : EXPOSE 8080
 ---> Running in b0464ee89cdf
Removing intermediate container b0464ee89cdf
 ---> 921f3de81528
Step 13/13 : ENTRYPOINT ["python", "recommendation_server.py"]
 ---> Running in 8d632ed55a9a
Removing intermediate container 8d632ed55a9a
 ---> b081f471e225
Successfully built b081f471e225
Successfully tagged mwanthi/recommendationservice:latest
[Pipeline] sh
+ docker tag mwanthi/recommendationservice mwanthi/recommendationservice:v0.0.1
[Pipeline] sh
+ docker push mwanthi/recommendationservice:v0.0.1
The push refers to repository [docker.io/mwanthi/recommendationservice]
840c6e0084cf: Preparing
d7d43df37daf: Preparing
cbdf52ef6dce: Preparing
e2bc26829d40: Preparing
6102c39d73fe: Preparing
462eacda1a69: Preparing
8d853c8add5d: Preparing
462eacda1a69: Waiting
8d853c8add5d: Waiting
e2bc26829d40: Mounted from mwanthi/loadgenerator
6102c39d73fe: Mounted from mwanthi/loadgenerator
462eacda1a69: Mounted from mwanthi/loadgenerator
840c6e0084cf: Pushed
8d853c8add5d: Mounted from mwanthi/loadgenerator
cbdf52ef6dce: Pushed
d7d43df37daf: Pushed
v0.0.1: digest: sha256:b0e2388fb43cf4a7b2cf97f7c30092dff70677e3a45f9433e2f0394ef3183f61 size: 1786
[Pipeline] sh
+ docker push mwanthi/recommendationservice:latest
The push refers to repository [docker.io/mwanthi/recommendationservice]
840c6e0084cf: Preparing
d7d43df37daf: Preparing
cbdf52ef6dce: Preparing
e2bc26829d40: Preparing
6102c39d73fe: Preparing
462eacda1a69: Preparing
8d853c8add5d: Preparing
8d853c8add5d: Waiting
462eacda1a69: Waiting
6102c39d73fe: Layer already exists
840c6e0084cf: Layer already exists
e2bc26829d40: Layer already exists
d7d43df37daf: Layer already exists
cbdf52ef6dce: Layer already exists
462eacda1a69: Layer already exists
8d853c8add5d: Layer already exists
latest: digest: sha256:b0e2388fb43cf4a7b2cf97f7c30092dff70677e3a45f9433e2f0394ef3183f61 size: 1786
[Pipeline] sh
+ sed -i  -e s|mwanthi/recommendationservice:v0.0.1|mwanthi/recommendationservice:v0.0.1|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/recommendationservice/recommendationservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/recommendationservice:latest
Untagged: mwanthi/recommendationservice:latest
[Pipeline] sh
+ docker rmi mwanthi/recommendationservice:v0.0.1
Untagged: mwanthi/recommendationservice:v0.0.1
Untagged: mwanthi/recommendationservice@sha256:b0e2388fb43cf4a7b2cf97f7c30092dff70677e3a45f9433e2f0394ef3183f61
Deleted: sha256:b081f471e225deec0322ce936cbe4fafd64970624b3cfc81968ec5e824766505
Deleted: sha256:921f3de815281baf1c145eff962cab5a5f5bb55a0f62a043bb5d30ebdb0dc6e2
Deleted: sha256:fa6f2c6c809ae04862e23ca5f36e845aca51630ed0f2e69c25cc79f67523cd7b
Deleted: sha256:9ed270b19a837d62efa0eef2b48afa9489433b809209e0ac3901a13ce0209086
Deleted: sha256:22d0f3dacecaca1ca2a14445dca77389bd20d82617de31edcb874a0d8ac8fa84
Deleted: sha256:1e673499e1160ff319e06da89bd25113ae583a038cd588c5c8938ab666c16664
Deleted: sha256:fdf94fe8fbfdd7f23e959e636075d766b5a65c5b7ff546c417a06049bb92480b
Deleted: sha256:e1e12f824c6a04ce3d72ff94946cbed7b04fd1b914815e49a00d504d9fe188f2
Deleted: sha256:988371913d2fcf14d6a37a33cc0cd2dca319ae59769cd80fdedd281beea3c028
Deleted: sha256:cc21335e30feeca3ad453c034d98adb21b59e40dce0c7626aba833d209161e32
[Pipeline] sh
+ docker image prune -f
Deleted Images:
deleted: sha256:e2e469875770c0592cf4a6ab126d4d9c62085ecc85b78b25defdbf9c4dc61645
deleted: sha256:2677bfd2f99f708d263eaee73b8fcea996d04dba113519c11f910844834fc168
deleted: sha256:243796190c0bce251950da2f2ddefafa215eefb1125517a6aa9d5f6ea230e1a4
deleted: sha256:a674db094233597707d55b6dbf4624c02e5e12a45f6b7f8306c3baf5f6261489
deleted: sha256:80b3f931c8df9c7c274f32a707de421aa0cc2de0d7de5bff1b02a07c38bfde66
deleted: sha256:8b9f2cf6aad6539326ac4dfc0da5b20c80470e668932e4be013655ec13daeccb
untagged: golang@sha256:ac67716dd016429be8d4c2c53a248d7bcdf06d34127d3dc451bda6aa5a87bc06
deleted: sha256:b5ada884192f173018fcb39688bd70545669ab105941231067ea5dbed4ac6914
deleted: sha256:2968ff6a64392cda70b3e2cb5d6e62723bfdc18fe68b46382c971bee002890a2
deleted: sha256:768a08d8d838830bce342fdf82d2051ad375b9a575cb6cb685f8841bc16f5ae2
deleted: sha256:7c37ab7540e48469f2843766943fb1f5b838efe35a1e500268f45f1b6ba88942
deleted: sha256:db287705205f639bdfff0f98a53c5b40608826ee5ab2b1180bcf22eec319953c
deleted: sha256:63ca1fbb43ae5034640e5e6cb3e083e05c290072c5366fcaa9d62435a4cced85

Total reclaimed space: 652MB
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // withDockerRegistry
[Pipeline] }
[Pipeline] // script
[Pipeline] echo
Tracking and building shippingservice service...
[Pipeline] sh
+ echo shippingservice
[Pipeline] script
[Pipeline] {
[Pipeline] echo
Building and Pushing shippingservice image....
[Pipeline] withDockerRegistry
$ docker login -u mwanthi -p ******** https://index.docker.io/v1/
WARNING! Using --password via the CLI is insecure. Use --password-stdin.
WARNING! Your password will be stored unencrypted in /home/ubuntu/workspace/microservices-build@tmp/3686c69c-ff8c-407a-a135-5c95bba4984a/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
[Pipeline] {
[Pipeline] sh
+ grep image: mwanthi/shippingservice:[^[:space:]]* /home/ubuntu/workspace/microservices-build/kubernetes-manifests/shippingservice/shippingservice.yaml
+ awk -F : {print $3}
+ awk {gsub(/^v/, ""); print}
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
Step 2/14 : WORKDIR /src
 ---> Running in a394d81e1a2f
Removing intermediate container a394d81e1a2f
 ---> a20732ab86d4
Step 3/14 : COPY go.mod go.sum ./
 ---> b2fa030016d5
Step 4/14 : RUN go mod download
 ---> Running in 1f700cbad6e2
Removing intermediate container 1f700cbad6e2
 ---> a373670d8c07
Step 5/14 : COPY . .
 ---> b1f170989e1b
Step 6/14 : ARG SKAFFOLD_GO_GCFLAGS
 ---> Running in 7c394fd85a65
Removing intermediate container 7c394fd85a65
 ---> d57697013d90
Step 7/14 : RUN CGO_ENABLED=0 GOOS=linux go build -gcflags="${SKAFFOLD_GO_GCFLAGS}" -o /go/bin/shippingservice .
 ---> Running in 8a41e216a397
Removing intermediate container 8a41e216a397
 ---> fee72edad63a
Step 8/14 : FROM scratch
 ---> 
Step 9/14 : WORKDIR /src
 ---> Running in 6e49f7e3a961
Removing intermediate container 6e49f7e3a961
 ---> da4e759b71e8
Step 10/14 : COPY --from=builder /go/bin/shippingservice /src/shippingservice
 ---> c678d7bb28bb
Step 11/14 : ENV APP_PORT=50051
 ---> Running in 8f0eda140e9c
Removing intermediate container 8f0eda140e9c
 ---> 02c3b756838f
Step 12/14 : ENV GOTRACEBACK=single
 ---> Running in 4f6ebbfc5bec
Removing intermediate container 4f6ebbfc5bec
 ---> d930c8faec53
Step 13/14 : EXPOSE 50051
 ---> Running in f006fac4b39f
Removing intermediate container f006fac4b39f
 ---> fd5b2ab82e65
Step 14/14 : ENTRYPOINT ["/src/shippingservice"]
 ---> Running in 425cab0f6b72
Removing intermediate container 425cab0f6b72
 ---> 6b54dee6105d
Successfully built 6b54dee6105d
Successfully tagged mwanthi/shippingservice:latest
[Pipeline] sh
+ docker tag mwanthi/shippingservice mwanthi/shippingservice:v0.0.1
[Pipeline] sh
+ docker push mwanthi/shippingservice:v0.0.1
The push refers to repository [docker.io/mwanthi/shippingservice]
91b465b30e3c: Preparing
4fa42f130958: Preparing
4fa42f130958: Pushed
91b465b30e3c: Pushed
v0.0.1: digest: sha256:8cbdf3d38b9ceb6d7ec8e4f16d978fbb723acd5d542080ae31f3f47265a61c24 size: 735
[Pipeline] sh
+ docker push mwanthi/shippingservice:latest
The push refers to repository [docker.io/mwanthi/shippingservice]
91b465b30e3c: Preparing
4fa42f130958: Preparing
4fa42f130958: Layer already exists
91b465b30e3c: Layer already exists
latest: digest: sha256:8cbdf3d38b9ceb6d7ec8e4f16d978fbb723acd5d542080ae31f3f47265a61c24 size: 735
[Pipeline] sh
+ sed -i  -e s|mwanthi/shippingservice:v0.0.1|mwanthi/shippingservice:v0.0.1|g /home/ubuntu/workspace/microservices-build/kubernetes-manifests/shippingservice/shippingservice.yaml
sed: can't read : No such file or directory
+ true
[Pipeline] sh
+ docker rmi mwanthi/shippingservice:latest
Untagged: mwanthi/shippingservice:latest
[Pipeline] sh
+ docker rmi mwanthi/shippingservice:v0.0.1
Untagged: mwanthi/shippingservice:v0.0.1
Untagged: mwanthi/shippingservice@sha256:8cbdf3d38b9ceb6d7ec8e4f16d978fbb723acd5d542080ae31f3f47265a61c24
Deleted: sha256:6b54dee6105d96cf3eaba94215d9ecbe3590b422eb8ac2cf7ebcacb5e074cb86
Deleted: sha256:fd5b2ab82e65783c3fae073b9b70514b048f72fd8dba5736b78f94a5faeeeb3c
Deleted: sha256:d930c8faec53b329087dce17c020276f6f446a8e60a0dd58f1b901f193984449
Deleted: sha256:02c3b756838fa4b0c08260a786f5a87f39e9cea72ad00b5dd146f7890c49ced3
Deleted: sha256:c678d7bb28bbd60f73fb381512019d9ce4909b5b4b07ba9c4713dc5193a287c8
Deleted: sha256:2310490b08fbfacbd41d33bccedde6b1f3db83632502fdc8d7e618932b8f3fe5
Deleted: sha256:da4e759b71e8ec7d31c91be31e9f432da2ab0f3034de24f787224915c0368d42
Deleted: sha256:4fa42f130958e7da9465a75de3537b437a7c56db0ded243ad2fab99e56185d98
[Pipeline] sh
+ docker image prune -f
Deleted Images:
untagged: python@sha256:ad48727987b259854d52241fac3bc633574364867b8e20aec305e6e7f4028b26
deleted: sha256:86b8b6de4ba2edaa00b6721a7d77a19dc0b20642af20f772b71152fda8d5a3a8
deleted: sha256:06cd4d7df090c22215821a922931f3b2063b7540b1a380407c764a102b128491
deleted: sha256:74a2d6d826bd4906ec5ea1b9b11e1a01f5d2053a86165d59badf7a3677741847
deleted: sha256:0e0d8c7ac030d9d8fad72239164c1f2fde61d0590c35a4c07c4a2f3aa027baaf
deleted: sha256:8d853c8add5d1e7b0aafc4b68a3d9fb8e7a0da27970c2acf831fe63be4a0cd2c
deleted: sha256:fee72edad63afe0996fea210e8746775148406ea823e83570bf02acd253b3549
deleted: sha256:be1a3c1271cafe171d2467db2065f51709c03a87b57e45f762e04d26a6604052
deleted: sha256:d57697013d909ec69ff5eefee71b37c31882d874970c41e3b7d0b225d2ecbe81
deleted: sha256:b1f170989e1b50b2cede434a14d805cede7cc3e8670f88c521c8972b368765d1
deleted: sha256:97e8ff3cc990701382f23ef287f5b3a218d3b0653d91d60e30f6b95bacf80f4c
deleted: sha256:a373670d8c07db326a67172c1f68612b909f86000061be428193a7e090db5168
deleted: sha256:beb245a96be518b15ca3495a3999aeb6873ee828811a608231aa6a6fdcfd1f7e
deleted: sha256:b2fa030016d5189142c2563698db13a0332c6a4225247b04ea5fb44e193c8deb
deleted: sha256:79d8ef00a798cc5976ae80649a42c5b79f9d4259aa960bcedddbc5225f020a1e
deleted: sha256:a20732ab86d48c4f021bc15446f2a968e0d32186dc455f83d41e93d29ad0b7dc
deleted: sha256:469c2858dcdcadcb1adcd04224da115f4381dd9191521e45f3ded42e2feb82f8

Total reclaimed space: 848.1MB
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
+ git commit -m Updated Deployment Manifest-Build 1
[main 073329f] Updated Deployment Manifest-Build 1
 12 files changed, 0 insertions(+), 0 deletions(-)
 mode change 100644 => 100755 README.md
 mode change 100644 => 100755 adservice/adservice.yaml
 mode change 100644 => 100755 cartservice/cartservice.yaml
 mode change 100644 => 100755 checkoutservice/checkoutservice.yaml
 mode change 100644 => 100755 currencyservice/currencyservice.yaml
 mode change 100644 => 100755 emailservice/emailservice.yaml
 mode change 100644 => 100755 frontend/frontend.yaml
 mode change 100644 => 100755 loadgenerator/loadgenerator.yaml
 mode change 100644 => 100755 paymentservice/paymentservice.yaml
 mode change 100644 => 100755 productcatalogservice/productcatalogservice.yaml
 mode change 100644 => 100755 recommendationservice/recommendationservice.yaml
 mode change 100644 => 100755 shippingservice/shippingservice.yaml
[Pipeline] withCredentials
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
Masking supported pattern matches of $GIT_PASSWORD or $GIT_ASKPASS
[Pipeline] {
[Pipeline] sh
+ git push https://github.com/D-Mwanth/kubernetes-manifests.git main
To https://github.com/D-Mwanth/kubernetes-manifests.git
   65bcf89..073329f  main -> main
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