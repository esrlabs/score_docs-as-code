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
load("//:docs.bzl", "docs")

# Creates all documentation targets:
# - `docs:incremental` for building docs incrementally at runtime
# - `docs:live_preview` for live preview in the browser without an IDE
# - `docs:ide_support` for creating python virtualenv for IDE support
# - `docs:docs` for building documentation at build-time

docs(
    conf_dir = "docs",
    docs_targets = [
        {
            "suffix": "latest",  # latest main branch documentation build
            "external_needs_info": [
                {
                    "base_url": "https://eclipse-score.github.io/process_description/main",
                    "json_url": "https://eclipse-score.github.io/process_description/main/needs.json",
                    "id_prefix": "process_",
                },
            ],
        },
        {
            "suffix": "release",  # The version imported from MODULE.bazel
            "target": [
                "@score_process//process:docs_needs_latest",
            ],
            "external_needs_info": [
                {
                    "base_url": "https://eclipse-score.github.io/process_description/main",
                    "json_path": "/score_process~/process/docs_needs_latest/_build/needs/needs.json",
                    "id_prefix": "process_",
                },
            ],
        },
    ],
    source_dir = "docs",
)
