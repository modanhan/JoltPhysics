load("@rules_cc//cc:defs.bzl", "cc_import", "cc_library")

cc_import(
    name = "vulkan_windows_private",
    hdrs = glob([
        "Include/**/*.hpp",
        "Include/**/*.h",
    ]),
    static_library = "Lib/vulkan-1.lib",
    visibility = ["//visibility:public"],
)

cc_library(
    name = "vulkan_windows",
    hdrs = glob([
        "Include/**/*.hpp",
        "Include/**/*.h",
    ]),
    strip_include_prefix = "Include",
    visibility = ["//visibility:public"],
    deps = [":vulkan_windows_private"],
)
