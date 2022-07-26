```bash
ansible-playbook playbook.yml --ask-vault-pass
```

```bash
Vault password:

PLAY [Jenkins Build] ********************************************************************************************************************************************************************************

TASK [Gathering Facts] ******************************************************************************************************************************************************************************
ok: [jenkins_server_1]

TASK [jenkins_build : Add Jenkins repository] *******************************************************************************************************************************************************
ok: [jenkins_server_1] => (item=jenkins_server_1)

TASK [jenkins_build : Import Jenkins Key] ***********************************************************************************************************************************************************
ok: [jenkins_server_1]

TASK [jenkins_build : Install Jenkins and Java] *****************************************************************************************************************************************************
ok: [jenkins_server_1]

TASK [jenkins_build : Just force systemd to reread configs] *****************************************************************************************************************************************
ok: [jenkins_server_1]

TASK [jenkins_build : Start and Enable Jenkins service] *********************************************************************************************************************************************
ok: [jenkins_server_1]

TASK [jenkins_build : Set defaults for Jenkins] *****************************************************************************************************************************************************
ok: [jenkins_server_1]

TASK [jenkins_build : Create init folder] ***********************************************************************************************************************************************************
ok: [jenkins_server_1]

TASK [jenkins_build : Set username and password] ****************************************************************************************************************************************************
ok: [jenkins_server_1]

TASK [jenkins_build : Restart and Enable Jenkins service] *******************************************************************************************************************************************
changed: [jenkins_server_1]

TASK [jenkins_build : Get the Jenkins Plugin] *******************************************************************************************************************************************************
ok: [jenkins_server_1]

TASK [jenkins_build : Set username and password for Jenkins Plugin] *********************************************************************************************************************************
ok: [jenkins_server_1]

TASK [jenkins_build : Install Plugins] **************************************************************************************************************************************************************
changed: [jenkins_server_1]

TASK [jenkins_build : Copy Job Template] ************************************************************************************************************************************************************
ok: [jenkins_server_1]

TASK [jenkins_build : Create Job Template] **********************************************************************************************************************************************************
changed: [jenkins_server_1]

TASK [jenkins_build : Restart and Enable Jenkins service] *******************************************************************************************************************************************
changed: [jenkins_server_1]

TASK [jenkins_build : Get Initial Admin Password file] **********************************************************************************************************************************************
changed: [jenkins_server_1]

TASK [jenkins_build : debug] ************************************************************************************************************************************************************************
ok: [jenkins_server_1] => {
    "msg": [
        "Jenkins initial Admin Password: 017d1f3aefa64dd392ca69820655bce7"
    ]
}

PLAY RECAP ******************************************************************************************************************************************************************************************
jenkins_server_1           : ok=18   changed=5    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```
