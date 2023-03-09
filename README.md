This playbook uses:
lshw 
nvme-cli
smartmontools


Check the playbook:
```
$ yamllint playbook.yaml 
$ ansible-lint playbook.yaml 
$ ansible-playbook --syntax-check -i hosts playbook.yaml  
```
And run:
```
$ ansible-playbook -i hosts --private-key ~/.ssh/ansible_id_rsa -u ansible playbook.yaml
```

Results:
```
ok: [k8s-n3.google.com] => {
    "msg": [
        "- '         ProLiant DL360 Gen9 (755258-B21)'",
        "- '      1  192GiB System Memory'",
        "- '      6  32GiB DIMM DDR4 Synchronous LRDIMM 2133 MHz (0.5 ns)'",
        "- '      2  Intel(R) Xeon(R) CPU E5-2680 v4 @ 2.40GHz'",
        "- '      1 Micron_9300_MTFDHAL7T6TDP'",
        "- '      2  SAMSUNG MZ7LH480HAHQ-00005'",
        "- '----------lsblk---------'",
        "- NAME    MODEL                      SERIAL           SIZE",
        "- sda     SAMSUNG_MZ7LH480HAHQ-00005 S45PNC0R310139 447.1G",
        "- sdb     SAMSUNG_MZ7LH480HAHQ-00005 S45PNC0R310138 447.1G",
        "- nvme0n1 Micron_9300_MTFDHAL7T6TDP  20512BF40FF0       7T",
        ""
    ]
}
```
