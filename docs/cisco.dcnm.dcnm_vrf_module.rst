.. _cisco.dcnm.dcnm_vrf_module:


*******************
cisco.dcnm.dcnm_vrf
*******************

**Add and remove VRFs from a DCNM managed VXLAN fabric.**


Version added: 0.9.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- Add and remove VRFs and VRF Lite Extension from a DCNM managed VXLAN fabric.
- In Multisite fabrics, VRFs can be created only on Multisite fabric
- In Multisite fabrics, VRFs cannot be created on member fabric




Parameters
----------

.. raw:: html

    <table  border=0 cellpadding=0 class="documentation-table">
        <tr>
            <th colspan="5">Parameter</th>
            <th>Choices/<font color="blue">Defaults</font></th>
            <th width="100%">Comments</th>
        </tr>
            <tr>
                <td colspan="5">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>config</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">list</span>
                         / <span style="color: purple">elements=dictionary</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>List of details of vrfs being managed. Not required for state deleted</div>
                </td>
            </tr>
                                <tr>
                    <td class="elbow-placeholder"></td>
                <td colspan="4">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>attach</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">list</span>
                         / <span style="color: purple">elements=dictionary</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>List of vrf attachment details</div>
                </td>
            </tr>
                                <tr>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                <td colspan="3">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>deploy</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">boolean</span>
                    </div>
                </td>
                <td>
                        <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                    <li>no</li>
                                    <li><div style="color: blue"><b>yes</b>&nbsp;&larr;</div></li>
                        </ul>
                </td>
                <td>
                        <div>Per switch knob to control whether to deploy the attachment</div>
                        <div>This knob has been deprecated from Ansible NDFC Collection Version 2.1.0 onwards. There will not be any functional impact if specified in playbook.</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                <td colspan="3">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>ip_address</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                         / <span style="color: red">required</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>IP address of the switch where vrf will be attached or detached</div>
                </td>
            </tr>
                                <tr>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>vrf_lite</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">list</span>
                         / <span style="color: purple">elements=dictionary</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>VRF Lite Extensions options</div>
                </td>
            </tr>
                                <tr>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>dot1q</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>DOT1Q Id</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>interface</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>Interface of the switch which is connected to the edge router</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>ipv4_addr</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>IP address of the interface which is connected to the edge router</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>ipv6_addr</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>IPv6 address of the interface which is connected to the edge router</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>neighbor_ipv4</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>Neighbor IP address of the edge router</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>neighbor_ipv6</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>Neighbor IPv6 address of the edge router</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                    <td class="elbow-placeholder"></td>
                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>peer_vrf</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                         / <span style="color: red">required</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>VRF Name to which this extension is attached</div>
                </td>
            </tr>



            <tr>
                    <td class="elbow-placeholder"></td>
                <td colspan="4">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>deploy</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">boolean</span>
                    </div>
                </td>
                <td>
                        <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                    <li>no</li>
                                    <li><div style="color: blue"><b>yes</b>&nbsp;&larr;</div></li>
                        </ul>
                </td>
                <td>
                        <div>Global knob to control whether to deploy the attachment</div>
                        <div>Ansible NDFC Collection Behavior for Version 2.0.1 and earlier</div>
                        <div>This knob will create and deploy the attachment in DCNM only when set to &quot;True&quot; in playbook</div>
                        <div>Ansible NDFC Collection Behavior for Version 2.1.0 and later</div>
                        <div>Attachments specified in the playbook will always be created in DCNM. This knob, when set to &quot;True&quot;,  will deploy the attachment in DCNM, by pushing the configs to switch. If set to &quot;False&quot;, the attachments will be created in DCNM, but will not be deployed</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                <td colspan="4">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>service_vrf_template</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                    </div>
                </td>
                <td>
                        <b>Default:</b><br/><div style="color: blue">"None"</div>
                </td>
                <td>
                        <div>Service vrf template</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                <td colspan="4">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>vlan_id</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">integer</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>vlan ID for the vrf attachment</div>
                        <div>If not specified in the playbook, DCNM will auto-select an available vlan_id</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                <td colspan="4">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>vrf_extension_template</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                    </div>
                </td>
                <td>
                        <b>Default:</b><br/><div style="color: blue">"Default_VRF_Extension_Universal"</div>
                </td>
                <td>
                        <div>Name of the extension config template to be used</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                <td colspan="4">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>vrf_id</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">integer</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>ID of the vrf being managed</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                <td colspan="4">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>vrf_name</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                         / <span style="color: red">required</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>Name of the vrf being managed</div>
                </td>
            </tr>
            <tr>
                    <td class="elbow-placeholder"></td>
                <td colspan="4">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>vrf_template</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                    </div>
                </td>
                <td>
                        <b>Default:</b><br/><div style="color: blue">"Default_VRF_Universal"</div>
                </td>
                <td>
                        <div>Name of the config template to be used</div>
                </td>
            </tr>

            <tr>
                <td colspan="5">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>fabric</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                         / <span style="color: red">required</span>
                    </div>
                </td>
                <td>
                </td>
                <td>
                        <div>Name of the target fabric for vrf operations</div>
                </td>
            </tr>
            <tr>
                <td colspan="5">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>state</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                    </div>
                </td>
                <td>
                        <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                    <li><div style="color: blue"><b>merged</b>&nbsp;&larr;</div></li>
                                    <li>replaced</li>
                                    <li>overridden</li>
                                    <li>deleted</li>
                                    <li>query</li>
                        </ul>
                </td>
                <td>
                        <div>The state of DCNM after module completion.</div>
                </td>
            </tr>
    </table>
    <br/>




Examples
--------

.. code-block:: yaml

    # This module supports the following states:
    #
    # Merged:
    #   VRFs defined in the playbook will be merged into the target fabric.
    #     - If the VRF does not exist it will be added.
    #     - If the VRF exists but properties managed by the playbook are different
    #       they will be updated if possible.
    #     - VRFs that are not specified in the playbook will be untouched.
    #
    # Replaced:
    #   VRFs defined in the playbook will be replaced in the target fabric.
    #     - If the VRF does not exist it will be added.
    #     - If the VRF exists but properties managed by the playbook are different
    #       they will be updated if possible.
    #     - Properties that can be managed by the module but are  not specified
    #       in the playbook will be deleted or defaulted if possible.
    #     - VRFs that are not specified in the playbook will be untouched.
    #
    # Overridden:
    #   VRFs defined in the playbook will be overridden in the target fabric.
    #     - If the VRF does not exist it will be added.
    #     - If the VRF exists but properties managed by the playbook are different
    #       they will be updated if possible.
    #     - Properties that can be managed by the module but are not specified
    #       in the playbook will be deleted or defaulted if possible.
    #     - VRFs that are not specified in the playbook will be deleted.
    #
    # Deleted:
    #   VRFs defined in the playbook will be deleted.
    #   If no VRFs are provided in the playbook, all VRFs present on that DCNM fabric will be deleted.
    #
    # Query:
    #   Returns the current DCNM state for the VRFs listed in the playbook.
    #
    # rollback functionality:
    # This module supports task level rollback functionality. If any task runs into failures, as part of failure
    # handling, the module tries to bring the state of the DCNM back to the state captured in have structure at the
    # beginning of the task execution. Following few lines provide a logical description of how this works,
    # if (failure)
    #     want data = have data
    #     have data = get state of DCNM
    #     Run the module in override state with above set of data to produce the required set of diffs
    #     and push the diff payloads to DCNM.
    # If rollback fails, the module does not attempt to rollback again, it just quits with appropriate error messages.

    # The two VRFs below will be merged into the target fabric.
    - name: Merge vrfs
      cisco.dcnm.dcnm_vrf:
        fabric: vxlan-fabric
        state: merged
        config:
        - vrf_name: ansible-vrf-r1
          vrf_id: 9008011
          vrf_template: Default_VRF_Universal
          vrf_extension_template: Default_VRF_Extension_Universal
          vlan_id: 2000
          service_vrf_template: null
          attach:
          - ip_address: 192.168.1.224
            deploy: true
          - ip_address: 192.168.1.225
            deploy: false
        - vrf_name: ansible-vrf-r2
          vrf_id: 9008012
          vrf_template: Default_VRF_Universal
          vrf_extension_template: Default_VRF_Extension_Universal
          service_vrf_template: null
          attach:
          - ip_address: 192.168.1.224
          - ip_address: 192.168.1.225

    # VRF LITE Extension attached
    - name: Merge vrfs
      cisco.dcnm.dcnm_vrf:
        fabric: vxlan-fabric
        state: merged
        config:
        - vrf_name: ansible-vrf-r1
          vrf_id: 9008011
          vrf_template: Default_VRF_Universal
          vrf_extension_template: Default_VRF_Extension_Universal
          vlan_id: 2000
          service_vrf_template: null
          attach:
          - ip_address: 192.168.1.224
          - ip_address: 192.168.1.225
            vrf_lite:
             # All parameters under vrf_lite except peer_vrf are optional and
             # will be supplied by DCNM when omitted in the playbook
              - peer_vrf: test_vrf_1 # peer_vrf is mandatory
                interface: Ethernet1/16 # optional
                ipv4_addr: 10.33.0.2/30 # optional
                neighbor_ipv4: 10.33.0.1 # optional
                ipv6_addr: 2010::10:34:0:7/64 # optional
                neighbor_ipv6: 2010::10:34:0:3 # optional
                dot1q: 2 # dot1q can be got from dcnm/optional

    # The two VRFs below will be replaced in the target fabric.
    - name: Replace vrfs
      cisco.dcnm.dcnm_vrf:
        fabric: vxlan-fabric
        state: replaced
        config:
        - vrf_name: ansible-vrf-r1
          vrf_id: 9008011
          vrf_template: Default_VRF_Universal
          vrf_extension_template: Default_VRF_Extension_Universal
          vlan_id: 2000
          service_vrf_template: null
          attach:
          - ip_address: 192.168.1.224
            deploy: true
          # Delete this attachment
          # - ip_address: 192.168.1.225
          # deploy: true
          # Create the following attachment
          - ip_address: 192.168.1.226
            deploy: true
        # Dont touch this if its present on DCNM
        # - vrf_name: ansible-vrf-r2
        #   vrf_id: 9008012
        #   vrf_template: Default_VRF_Universal
        #   vrf_extension_template: Default_VRF_Extension_Universal
        #   attach:
        #   - ip_address: 192.168.1.224
        #   - ip_address: 192.168.1.225

    # The two VRFs below will be overridden in the target fabric.
    - name: Override vrfs
      cisco.dcnm.dcnm_vrf:
        fabric: vxlan-fabric
        state: overridden
        config:
        - vrf_name: ansible-vrf-r1
          vrf_id: 9008011
          vrf_template: Default_VRF_Universal
          vrf_extension_template: Default_VRF_Extension_Universal
          vlan_id: 2000
          service_vrf_template: null
          attach:
          - ip_address: 192.168.1.224
            deploy: true
          # Delete this attachment
          # - ip_address: 192.168.1.225
          #   deploy: true
          # Create the following attachment
          - ip_address: 192.168.1.226
            deploy: true
        # Delete this vrf
        # - vrf_name: ansible-vrf-r2
        #   vrf_id: 9008012
        #   vrf_template: Default_VRF_Universal
        #   vrf_extension_template: Default_VRF_Extension_Universal
        #   vlan_id: 2000
        #   service_vrf_template: null
        #   attach:
        #   - ip_address: 192.168.1.224
        #   - ip_address: 192.168.1.225

    - name: Delete selected vrfs
      cisco.dcnm.dcnm_vrf:
        fabric: vxlan-fabric
        state: deleted
        config:
        - vrf_name: ansible-vrf-r1
          vrf_id: 9008011
          vrf_template: Default_VRF_Universal
          vrf_extension_template: Default_VRF_Extension_Universal
          vlan_id: 2000
          service_vrf_template: null
        - vrf_name: ansible-vrf-r2
          vrf_id: 9008012
          vrf_template: Default_VRF_Universal
          vrf_extension_template: Default_VRF_Extension_Universal
          vlan_id: 2000
          service_vrf_template: null

    - name: Delete all the vrfs
      cisco.dcnm.dcnm_vrf:
        fabric: vxlan-fabric
        state: deleted

    - name: Query vrfs
      cisco.dcnm.dcnm_vrf:
        fabric: vxlan-fabric
        state: query
        config:
        - vrf_name: ansible-vrf-r1
        - vrf_name: ansible-vrf-r2




Status
------


Authors
~~~~~~~

- Shrishail Kariyappanavar(@nkshrishail), Karthik Babu Harichandra Babu (@kharicha), Praveen Ramoorthy(@praveenramoorthy)
