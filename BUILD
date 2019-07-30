package(default_visibility = ["//visibility:public"])

java_library(
    name = "wc-common",
    srcs = glob(["wc-common/src/main/java/myproject/apache/beam/examples/*.java"]),
    deps = [
        "@maven//:org_apache_maven_surefire_maven-surefire-plugin",
        "@maven//:org_apache_maven_plugins_maven-compiler-plugin",
        "@maven//:org_codehaus_mojo_exec-maven-plugin",
        "@maven//:org_apache_beam_beam-runners-direct-java",
        "@maven//:org_apache_beam_beam-runners-reference-java",
        "@maven//:org_apache_beam_beam-runners-apex",
        "@maven//:org_apache_beam_beam-runners-google-cloud-dataflow-java",
        "@maven//:org_apache_beam_beam-sdks-java-io-google-cloud-platform",
        "@maven//:org_apache_beam_beam-runners-gearpump",
        "@maven//:org_apache_beam_beam-runners-samza",
        "@maven//:org_apache_beam_beam-sdks-java-core",
        "@maven//:org_apache_httpcomponents_httpclient",
        "@maven//:org_apache_hadoop_hadoop-yarn-client",
        "@maven//:org_apache_hadoop_hadoop-common",
        "@maven//:org_slf4j_slf4j-api",
        "@maven//:com_google_api-client_google-api-client",
        "@maven//:com_google_apis_google-api-services-bigquery",
        "@maven//:com_google_http-client_google-http-client",
        "@maven//:joda-time_joda-time",
        "@maven//:org_hamcrest_hamcrest-core",
        "@maven//:org_hamcrest_hamcrest-library",
        "@maven//:junit_junit",
        "@maven//:org_mockito_mockito-core",
    ]
)


java_binary(
    name = "wc1",
    srcs = glob(["wc1/src/*.java"]),
    main_class = "org.apache.beam.examples.WordCount",
    runtime_deps = [":wc-common"],
)

java_test(
    name = "tests",
    srcs = glob(["src/test/java/com/example/myproject/*.java"]),
    test_class = "com.example.myproject.TestApp",
    deps = [
        ":wc-common",
        "@com_google_guava_guava//jar",
    ],
)
