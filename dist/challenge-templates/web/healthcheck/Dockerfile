# Copyright 2020 Google LLC
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     https://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
FROM gcr.io/kctf-docker/healthcheck@sha256:33e4b50046701011d3f57d0e76fa0611ec4ca09556b6e15843bad1c2ed709302

COPY healthz.py /home/user/
COPY doit.py /home/user/
COPY run.sh /home/user/
COPY env /home/user/

CMD kctf_drop_privs /home/user/run.sh & /home/user/healthz.py
