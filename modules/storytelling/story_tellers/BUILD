load("@rules_cc//cc:defs.bzl", "cc_library")
load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "base_teller",
    hdrs = ["base_teller.h"],
    deps = [
        "//modules/common_msgs/storytelling_msgs:story_cc_proto",
    ],
)

cc_library(
    name = "close_to_junction_teller",
    srcs = ["close_to_junction_teller.cc"],
    hdrs = ["close_to_junction_teller.h"],
    deps = [
        ":base_teller",
        "//modules/common/adapters:adapter_gflags",
        "//modules/map/hdmap:hdmap_util",
        "//modules/common_msgs/planning_msgs:planning_cc_proto",
        "//modules/storytelling:frame_manager",
        "//modules/storytelling/common:storytelling_gflags",
        "//modules/storytelling/proto:storytelling_config_cc_proto",
    ],
)

cpplint()
