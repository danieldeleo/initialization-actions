package(default_visibility = ["//visibility:public"])

py_test(
    name = "test_rapids",
    size = "enormous",
    srcs = ["test_rapids.py"],
    data = ["rapids.sh"] + glob(["internal/*"]),
    local = True,
    shard_count = 1,
    deps = [
        ":verify_rapids",
        "//integration_tests:dataproc_test_case",
        "@io_abseil_py//absl/testing:parameterized",
    ],
)

py_library(
    name = "verify_rapids",
    testonly = True,
    srcs = ["verify_rapids.py"],
)
