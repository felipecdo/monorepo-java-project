load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_JVM_EXTERNAL_TAG = "2.0.1"
RULES_JVM_EXTERNAL_SHA = "55e8d3951647ae3dffde22b4f7f8dee11b3f70f3f89424713debd7076197eaca"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    name = "maven",
    artifacts = [
        "org.apache.maven.surefire:surefire-junit47:2.21.0",
        "org.apache.maven.plugins:maven-surefire-plugin:2.21.0",
        "org.codehaus.mojo:exec-maven-plugin:1.6.0",
        "org.apache.beam:beam-runners-direct-java:2.13.0",
        "org.apache.beam:beam-runners-reference-java:2.13.0",
        "org.apache.beam:beam-runners-apex:2.13.0",
        "org.apache.beam:beam-runners-google-cloud-dataflow-java:2.13.0",
        "org.apache.beam:beam-sdks-java-io-google-cloud-platform:2.13.0",
        "org.apache.beam:beam-runners-gearpump:2.13.0",
        "org.apache.beam:beam-runners-samza:2.13.0",
        "org.apache.beam:beam-sdks-java-core:2.13.0",
        "org.apache.beam:beam-runners-direct-java:2.13.0",
        "org.apache.httpcomponents:httpclient:4.3.6",
        "org.apache.hadoop:hadoop-yarn-client:2.7.3",
        "org.apache.hadoop:hadoop-common:2.7.3",
        "org.slf4j:slf4j-api:1.7.25",
        "com.google.api-client:google-api-client:1.27.0",
        "com.google.apis:google-api-services-bigquery:v2-rev20181104-1.27.0",
        "com.google.http-client:google-http-client:1.27.0",
        "joda-time:joda-time:2.10.1",
        "org.hamcrest:hamcrest-core:2.1",
        "org.hamcrest:hamcrest-library:2.1",
        "junit:junit:4.13-beta-1",
        "org.mockito:mockito-core:1.10.19",
    ],
    repositories = [
        "https://jcenter.bintray.com/",
        "https://repo1.maven.org/maven2",
        "https://repository.apache.org/content/repositories/snapshots/",
    ],
    fetch_sources = True,   # Fetch source jars. Defaults to False.
)