# *******************************************************************************
# Copyright (c) 2025 Contributors to the Eclipse Foundation
#
# See the NOTICE file(s) distributed with this work for additional
# information regarding copyright ownership.
#
# This program and the accompanying materials are made available under the
# terms of the Apache License Version 2.0 which is available at
# https://www.apache.org/licenses/LICENSE-2.0
#
# SPDX-License-Identifier: Apache-2.0
# *******************************************************************************
load("@aspect_rules_py//py:defs.bzl", "py_library")
load("@pip_process//:requirements.bzl", "all_requirements")

py_library(
    name = "score_layout",
    srcs = glob(
        ["*.py"],
    ),
    imports = ["."],
    visibility = ["//visibility:public"],
    # TODO: Figure out if all requirements are needed or if we can break it down a bit
    deps = all_requirements,
)
