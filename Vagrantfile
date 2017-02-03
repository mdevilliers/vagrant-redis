# -------------------------------------------------------------------
# Copyright (c) 2017 Mark deVilliers.  All Rights Reserved.
#
# This file is provided to you under the Apache License,
# Version 2.0 (the "License"); you may not use this file
# except in compliance with the License.  You may obtain
# a copy of the License at
#
#   http:#www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.
#
# -------------------------------------------------------------------

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty64"
#  config.vm.network :forwarded_port, guest: 6379, host: 6379
  config.vm.network "private_network", ip: "192.168.50.4"
  
  config.vm.provider :virtualbox do |vbox|
    vbox.customize ["modifyvm", :id, "--memory", 1024]
  end

  config.vm.provision :shell, :path => "init.sh"
end
