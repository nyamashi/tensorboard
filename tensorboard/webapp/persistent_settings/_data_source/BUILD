load("//tensorboard/defs:defs.bzl", "tf_ng_module")

package(default_visibility = ["//tensorboard:internal"])

tf_ng_module(
    name = "_data_source",
    srcs = [
        "persistent_settings_data_source.ts",
        "persistent_settings_data_source_module.ts",
    ],
    deps = [
        ":types",
        "//tensorboard/webapp/metrics:types",
        "@npm//@angular/core",
        "@npm//@ngrx/store",
        "@npm//rxjs",
    ],
)

tf_ng_module(
    name = "types",
    srcs = [
        "types.ts",
    ],
    deps = [
        "//tensorboard/webapp/metrics:types",
        "//tensorboard/webapp/metrics/views/card_renderer:scalar_card_types",
    ],
)

tf_ng_module(
    name = "testing",
    testonly = True,
    srcs = [
        "testing.ts",
    ],
    deps = [
        ":_data_source",
        ":types",
        "@npm//@angular/core",
        "@npm//@types/jasmine",
        "@npm//rxjs",
    ],
)

tf_ng_module(
    name = "_data_source_test_lib",
    testonly = True,
    srcs = [
        "persistent_settings_data_source_test.ts",
    ],
    deps = [
        ":_data_source",
        ":types",
        "//tensorboard/webapp/angular:expect_angular_core_testing",
        "//tensorboard/webapp/metrics:types",
        "//tensorboard/webapp/metrics/views/card_renderer:scalar_card_types",
        "@npm//@angular/core",
        "@npm//@types/jasmine",
        "@npm//rxjs",
    ],
)
