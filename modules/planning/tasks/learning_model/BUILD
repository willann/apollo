load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "learning_model_inference_task",
    srcs = ["learning_model_inference_task.cc"],
    hdrs = ["learning_model_inference_task.h"],
    copts = ["-DMODULE_NAME=\\\"planning\\\""],
    deps = [
        "//modules/common/status",
        "//modules/planning/common:frame",
        "//modules/planning/common:reference_line_info",
        "//modules/planning/learning_based/img_feature_renderer:birdview_img_feature_renderer",
        "//modules/planning/learning_based/model_inference:trajectory_imitation_inference",
        "//modules/planning/proto:learning_data_proto",
        "//modules/planning/proto:planning_config_proto",
        "//modules/planning/tasks:task",
    ],
)

cc_library(
    name = "learning_model_inference_trajectory_task",
    srcs = ["learning_model_inference_trajectory_task.cc"],
    hdrs = ["learning_model_inference_trajectory_task.h"],
    copts = ["-DMODULE_NAME=\\\"planning\\\""],
    deps = [
        "//modules/common/status",
        "//modules/planning/common:frame",
        "//modules/planning/common:reference_line_info",
        "//modules/planning/proto:planning_config_proto",
        "//modules/planning/tasks:task",
    ],
)

cc_test(
    name = "learning_model_inference_task_test",
    size = "small",
    srcs = ["learning_model_inference_task_test.cc"],
    deps = [
        "learning_model_inference_task",
        "@com_google_googletest//:gtest_main",
    ],
)

cc_test(
    name = "learning_model_inference_trajectory_task_test",
    size = "small",
    srcs = ["learning_model_inference_trajectory_task_test.cc"],
    deps = [
        "learning_model_inference_trajectory_task",
        "@com_google_googletest//:gtest_main",
    ],
)

cpplint()
