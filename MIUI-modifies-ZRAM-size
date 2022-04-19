# MIUI 12.5&13 修改 ZRAM 大小

配置文件在`/system/etc/perfinit.conf`

老机型可以尝试修改下`/system/etc/mcd_default.conf`的文件。

物理内存（8G）：对应的zram 大小（6G）

以`/system/etc/perfinit.conf`为例

```diff
"zram_size": {
     "def": "512",
     "2": 1024,
     "3": 1536,
     "4": 2252,
     "6": 4096,
+    "8": 5120,
-    "8": 6144,
     "10": 6144,
     "12": 6144
  }
```

下面是修改好的数据，8G 物理内存开 5G Zram

```json
{
    "common": {
        "swap_on": 1,
        "global_swappiness": 100,
        "page_cluster": -1,
        "zram_size": {
            "def": "512",
            "2": 1024,
            "3": 1536,
            "4": 2252,
            "6": 4096,
            "8": 5120,
            "10": 6144,
            "12": 6144
        },
        "extm_on": 1,
        "extm_size": {
            "def": 512,
            "high_device": 3072,
            "3+64": 1024,
            "4+64": 1024,
            "6+64": 1024,
            "4+128": 2048,
            "6+128": 2048
        },
        "extm_file": "/data/extm/extm_file",
        "dex2oat_threads": {
            "def": 1,
            "4": 3,
            "8": 6
        },
        "boot_dex2oat_threads": {
            "def": 1,
            "4": 3,
            "8": 6
        },
        "bg_dex2oat_threads": {
            "def": 1,
            "1": 1,
            "2": 2,
            "3": 3,
            "4": 4,
            "5": 5,
            "6": 6,
            "7": 7,
            "8": 8,
            "9": 9,
            "10": 10
        },
        "reclaim_on_start": {
            "def": 0
        },
        "swappiness_on_start": {
            "def": 100
        },
        "reclaim_on_launcher": {
            "def": 0,
            "1": 120,
            "2": 120
        },
        "swappiness_on_launcher": {
            "def": 100,
            "2": 200
        }
    },
    "dex2oat": [
        {
            "product_name": [
                "dandelion",
                "angelica",
                "cattail",
                "angelican",
                "willow",
                "ginkgo",
                "cannon",
                "cannong",
                "mojito",
                "sunny",
                "rainbow",
                "rosemary",
                "secret",
                "maltose",
                "biloba",
                "XIG02",
                "chopin",
                "camellia",
                "camellian",
                "selene"
            ],
            "dex2oat_threads": {
                "def": 4
            },
            "boot_dex2oat_threads": {
                "def": 6
            },
            "bg_dex2oat_threads": {
                "def": 4
            }
        },
        {
            "product_name": [
                "merlin",
                "merlinin",
                "merlinnfc",
                "lancelot",
                "shiva",
                "pine",
                "olive",
                "olivelite",
                "olivewood",
                "onc",
                "lavender",
                "violet",
                "laurus",
                "camellia",
                "camellian"
            ],
            "dex2oat_threads": {
                "def": 4
            },
            "boot_dex2oat_threads": {
                "def": 6
            },
            "bg_dex2oat_threads": {
                "def": 4
            }
        }
    ],
    "zram": [
        {
            "product_name": [""],
            "zram_size": {
                "def": 512,
                "2": 1024,
                "3": 2048,
                "4": 2252,
                "6": 4096,
                "8": 5120,
                "10": 6144,
                "12": 6144
            }
        }
    ]
}

```

