load("@rules_cc//cc:defs.bzl", "cc_binary", "cc_library")

cc_library(
    name = "this-works-1",
    srcs = None,
    hdrs = ["hello-greet.h"],
)

cc_library(
    name = "this-works-2",
    srcs = [],
    hdrs = ["hello-greet.h"],
)

filegroup(
    name = "one_file",
    srcs = ["hello-greet.cc"],
) 

cc_library(
    name = "this-works-3",
    srcs = ["one_file"],
    hdrs = ["hello-greet.h"],
)


filegroup(
    name = "no_files",
    srcs = [],
) 

cc_library(
    name = "this-blows-1",
    srcs = ["no_files"],
    hdrs = ["hello-greet.h"],
)




cc_library(
    name = "hello-greet",
    srcs = ["hello-greet.cc"],
    hdrs = ["hello-greet.h"],
)

cc_binary(
    name = "hello-world",
    srcs = ["hello-world.cc"],
    deps = [
        ":hello-greet",
    ],
)
