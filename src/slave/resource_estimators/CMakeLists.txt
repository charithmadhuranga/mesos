# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# THE FIXED RESOURCE ESTIMATOR.
###############################
# NOTE: This library uses underscores because of a hard-coded expectation of
# `src/tests/oversubscription_tests.cpp`.
add_library(fixed_resource_estimator fixed.cpp)
target_link_libraries(fixed_resource_estimator PRIVATE mesos)
install(
  TARGETS fixed_resource_estimator
  RUNTIME DESTINATION ${MESOS_INSTALL_RUNTIME}
  LIBRARY DESTINATION ${MESOS_INSTALL_LIBRARIES}
  ARCHIVE DESTINATION ${MESOS_INSTALL_LIBRARIES})
