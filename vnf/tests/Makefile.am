#
# Copyright 2017 Cisco Systems, Inc.
# 
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
# 
# http://www.apache.org/licenses/LICENSE-2.0
# 
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
# 

#vnf unit test
#AUTOMAKE_OPTIONS=subdir-objects

AM_CPPFLAGS = -I$(top_srcdir)/nfapi/inc -I$(top_srcdir)/nfapi/public_inc  -I$(top_srcdir)/common/public_inc -I$(top_srcdir)/vnf/public_inc $(CFLAGS_CUNIT) -Wall -Werror

check_PROGRAMS= test_vnf

test_vnf_SOURCES = vnf_cunit_main.c ../..//common/src/debug.c   
test_vnf_LDADD=$(top_builddir)/vnf/libnfapi_vnf.a $(top_builddir)/nfapi/libnfapi.a  -L$(libdir) -lpthread -lrt -lsctp -lz -lcunit

LOG_DRIVER = $(top_srcdir)/tap-driver.sh
TESTS=test_vnf
EXTRA_DIST = $(TESTS)

