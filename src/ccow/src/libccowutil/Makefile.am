##
## Copyright (c) 2015-2018 Nexenta Systems, inc.
##
## This file is part of EdgeFS Project
## (see https://github.com/Nexenta/edgefs).
##
## Licensed to the Apache Software Foundation (ASF) under one
## or more contributor license agreements.  See the NOTICE file
## distributed with this work for additional information
## regarding copyright ownership.  The ASF licenses this file
## to you under the Apache License, Version 2.0 (the
## "License"); you may not use this file except in compliance
## with the License.  You may obtain a copy of the License at
##
##   http://www.apache.org/licenses/LICENSE-2.0
##
## Unless required by applicable law or agreed to in writing,
## software distributed under the License is distributed on an
## "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
## KIND, either express or implied.  See the License for the
## specific language governing permissions and limitations
## under the License.
##
lib_LTLIBRARIES = libccowutil.la

libccowutil_la_SOURCES = json.c logger.c lfq.c hashtable.c util.c talloc.c skiplist.c ccowtp.c \
			b64.c msort.c
libccowutil_la_CFLAGS = -rdynamic
libccowutil_la_LDFLAGS = -lcrypto $(AM_LDFLAGS) -lm -luv -lnanomsg -lpthread \
		     -lssl -lcrypto $(ASAN_LIB) -lbacktrace

libccowutil_la_LIBADD = $(top_srcdir)/src/libcrypto/libcrypto.la
