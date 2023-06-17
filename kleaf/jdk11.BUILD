# Copyright (C) 2023 The Android Open Source Project
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#       http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

load("@bazel_tools//tools/jdk:local_java_repository.bzl", "local_java_runtime")

package(default_visibility = ["//visibility:public"])

java_runtime(
    name = "local_jdk_runtime",
    srcs = glob(["**"]),
    java_home = ".",
)

local_java_runtime(
    name = "local_jdk",
    java_home = None,
    runtime_name = ":local_jdk_runtime",
    version = "11",
)

filegroup(
    name = "jar",
    srcs = ["bin/jar"],
    data = [":local_jdk_runtime"],
)
