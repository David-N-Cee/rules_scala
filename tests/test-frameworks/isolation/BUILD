load("@rules_scala_annex//rules:scala.bzl", "scala_library", "scala_test")

scala_library(
    name = "global",
    srcs = ["Global.scala"],
    scala = "//scala:2_12",
)

scala_test(
    name = "classloader",
    srcs = ["Test.scala"],
    isolation = "classloader",
    scala = "//scala:2_12",
    deps = [
        ":global",
        "@annex_test//:org_specs2_specs2_common_2_12",
        "@annex_test//:org_specs2_specs2_core_2_12",
        "@annex_test//:org_specs2_specs2_matcher_2_12",
    ],
)

scala_test(
    name = "classloader-jvm",
    srcs = ["TestJvm.scala"],
    isolation = "classloader",
    scala = "//scala:2_12",
    deps = [
        "@annex_test//:org_specs2_specs2_common_2_12",
        "@annex_test//:org_specs2_specs2_core_2_12",
        "@annex_test//:org_specs2_specs2_matcher_2_12",
    ],
)

scala_test(
    name = "classloader-shared",
    srcs = ["Test.scala"],
    isolation = "classloader",
    scala = "//scala:2_12",
    shared_deps = [":global"],
    deps = [
        ":global",
        "@annex_test//:org_specs2_specs2_common_2_12",
        "@annex_test//:org_specs2_specs2_core_2_12",
        "@annex_test//:org_specs2_specs2_matcher_2_12",
    ],
)

scala_test(
    name = "none",
    srcs = ["Test.scala"],
    scala = "//scala:2_12",
    deps = [
        ":global",
        "@annex_test//:org_specs2_specs2_common_2_12",
        "@annex_test//:org_specs2_specs2_core_2_12",
        "@annex_test//:org_specs2_specs2_matcher_2_12",
    ],
)

scala_test(
    name = "none-jvm",
    srcs = ["TestJvm.scala"],
    isolation = "none",
    scala = "//scala:2_12",
    deps = [
        "@annex_test//:org_specs2_specs2_common_2_12",
        "@annex_test//:org_specs2_specs2_core_2_12",
        "@annex_test//:org_specs2_specs2_matcher_2_12",
    ],
)

scala_test(
    name = "process",
    srcs = ["Test.scala"],
    isolation = "process",
    scala = "//scala:2_12",
    deps = [
        ":global",
        "@annex_test//:org_specs2_specs2_common_2_12",
        "@annex_test//:org_specs2_specs2_core_2_12",
        "@annex_test//:org_specs2_specs2_matcher_2_12",
    ],
)

scala_test(
    name = "process-2_11",
    srcs = ["Test.scala"],
    isolation = "process",
    scala = "//scala:2_11",
    deps = [
        ":global",
        "@annex_test//:org_specs2_specs2_common_2_11",
        "@annex_test//:org_specs2_specs2_core_2_11",
        "@annex_test//:org_specs2_specs2_matcher_2_11",
    ],
)

scala_test(
    name = "process-jvm",
    srcs = ["TestJvm.scala"],
    isolation = "process",
    scala = "//scala:2_12",
    deps = [
        "@annex_test//:org_specs2_specs2_common_2_12",
        "@annex_test//:org_specs2_specs2_core_2_12",
        "@annex_test//:org_specs2_specs2_matcher_2_12",
    ],
)
