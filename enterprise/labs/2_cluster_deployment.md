```
{
  "timestamp" : "2017-03-08T10:05:06.144Z",
  "clusters" : [ {
    "name" : "tantalus1984",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_bind_wildcard",
            "value" : "true"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3157155020"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "dfs_datanode_use_datanode_hostname",
            "value" : "true"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_bind_wildcard",
            "value" : "true"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "1610612736"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_bind_wildcard",
            "value" : "true"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "1610612736"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_client_use_datanode_hostname",
          "value" : "true"
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "aGWKGMqemyMhT2oCVeqlmfIaUWTprv"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "XC3A2aJtfjshsRy9JA50QXLoSUeCrt"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "ZOQZCak554Jltq3Bl7Lqak8FfPRgIJ"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-2c31286b24af8b05a30991e52dfb7dfb",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-00e81d4f93ac9a05f566a0478aed8697",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "2a0a0720-5d03-47a8-af3e-0cebf21d50f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2of0qoua65kxpgraty376xy3"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-0cb32eb3d42e440f1c081df5edb82c80",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "b92816dd-e84a-45e6-b718-28f05bc745b0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6pakzgr7vsotfk82spgdhdu71"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-4f902a4cad09a2c58aa7a5431b4bbe8b",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "7db0df38-5dd4-4a05-9fef-d6bbc6b261ef"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9a53o20spzfynufic6uuylx5r"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-2c31286b24af8b05a30991e52dfb7dfb",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4ez14t9hlf5rqir644vap8tgq"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-efde8cb79c049128f5b47729daa4d2e2",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bhr1c5sg42gwt95gr42sypnlz"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-00e81d4f93ac9a05f566a0478aed8697",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "2a0a0720-5d03-47a8-af3e-0cebf21d50f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cbxukkabb98vmlfc3ztm9dy6p"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-2c31286b24af8b05a30991e52dfb7dfb",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8g4jjixrh895o4398o2ymqfpr"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-efde8cb79c049128f5b47729daa4d2e2",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "fekbdht278lmpll0nkcmfnxo"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-2c31286b24af8b05a30991e52dfb7dfb",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "19"
          }, {
            "name" : "role_jceks_password",
            "value" : "bpdwic86d1ivaabartvg10y72"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-efde8cb79c049128f5b47729daa4d2e2",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "30"
          }, {
            "name" : "role_jceks_password",
            "value" : "drr2s7eruk2zg94s4gj9i2jkr"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "52428800"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-00e81d4f93ac9a05f566a0478aed8697",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "2a0a0720-5d03-47a8-af3e-0cebf21d50f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7btyhmd0xjbntwzlketkv5j3v"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-2c31286b24af8b05a30991e52dfb7dfb",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cckvgv99v51dhv51kvpr2fbbi"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-efde8cb79c049128f5b47729daa4d2e2",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3wzg96skvje2x342v3anbfqrn"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "52428800"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "5192"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5192"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "LYQn9YXH1KdLdnk7Hpy1a9vK6DCi2g"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-2c31286b24af8b05a30991e52dfb7dfb",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "535wejkx2cau7ho6flez56hhv"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-00e81d4f93ac9a05f566a0478aed8697",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "2a0a0720-5d03-47a8-af3e-0cebf21d50f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "26b35c8x1l6ujbc11s1gz7yke"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-0cb32eb3d42e440f1c081df5edb82c80",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "b92816dd-e84a-45e6-b718-28f05bc745b0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4dfv7mgs3uy5cr5557pmb0etp"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-4f902a4cad09a2c58aa7a5431b4bbe8b",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "7db0df38-5dd4-4a05-9fef-d6bbc6b261ef"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ck42tyaahxwj1xnkzgxsp06q9"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-2c31286b24af8b05a30991e52dfb7dfb",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "46"
          }, {
            "name" : "role_jceks_password",
            "value" : "f0rv9nory65t2lqmdialsnhaq"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-efde8cb79c049128f5b47729daa4d2e2",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "45"
          }, {
            "name" : "role_jceks_password",
            "value" : "e8kicxrhyvgv8gm29qfszt1a0"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "spark_on_yarn",
      "type" : "SPARK_ON_YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SPARK_YARN_HISTORY_SERVER",
          "items" : [ {
            "name" : "history_server_max_heapsize",
            "value" : "67108864"
          } ]
        } ],
        "items" : [ {
          "name" : "yarn_service",
          "value" : "yarn"
        } ]
      },
      "roles" : [ {
        "name" : "spar40365358-SPARK_YARN_HISTORY_SERVER-2c31286b24af8b05a30991e52",
        "type" : "SPARK_YARN_HISTORY_SERVER",
        "hostRef" : {
          "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "oax485ynw09v64zkr6wdqcl5"
          } ]
        }
      }, {
        "name" : "spark_on_yarn-GATEWAY-00e81d4f93ac9a05f566a0478aed8697",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "2a0a0720-5d03-47a8-af3e-0cebf21d50f0"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "spark_on_yarn-GATEWAY-0cb32eb3d42e440f1c081df5edb82c80",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "b92816dd-e84a-45e6-b718-28f05bc745b0"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "spark_on_yarn-GATEWAY-2c31286b24af8b05a30991e52dfb7dfb",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "spark_on_yarn-GATEWAY-4f902a4cad09a2c58aa7a5431b4bbe8b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "7db0df38-5dd4-4a05-9fef-d6bbc6b261ef"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "spark_on_yarn-GATEWAY-efde8cb79c049128f5b47729daa4d2e2",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa"
        },
        "config" : {
          "items" : [ ]
        }
      } ],
      "displayName" : "Spark"
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "52428800"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "3048210432"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "3441269145"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "579"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-26-85.eu-central-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive_password"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "spark_on_yarn_service",
          "value" : "spark_on_yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-00e81d4f93ac9a05f566a0478aed8697",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "2a0a0720-5d03-47a8-af3e-0cebf21d50f0"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-0cb32eb3d42e440f1c081df5edb82c80",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "b92816dd-e84a-45e6-b718-28f05bc745b0"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-2c31286b24af8b05a30991e52dfb7dfb",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-4f902a4cad09a2c58aa7a5431b4bbe8b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "7db0df38-5dd4-4a05-9fef-d6bbc6b261ef"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-efde8cb79c049128f5b47729daa4d2e2",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-efde8cb79c049128f5b47729daa4d2e2",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3vy46qt067bjmvgqzexkq2nw3"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-efde8cb79c049128f5b47729daa4d2e2",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cuuudnpffwibcwmb116xjo69"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-26-85.eu-central-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie_password"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "52428800"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "spark_on_yarn_service",
          "value" : "spark_on_yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-efde8cb79c049128f5b47729daa4d2e2",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5znnp7yrdx1ftam9s5tkw4ier"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-26-85.eu-central-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "hue_password"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-2c31286b24af8b05a30991e52dfb7dfb"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-efde8cb79c049128f5b47729daa4d2e2",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "61xjwx5daj1cvd4ksru7pjj7q"
          }, {
            "name" : "secret_key",
            "value" : "9OugBdZDYBdiU8IMtZj9QNtuzzJBJa"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "sqoop_client",
      "type" : "SQOOP_CLIENT",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "sqoop_client-GATEWAY-2c31286b24af8b05a30991e52dfb7dfb",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
        },
        "config" : {
          "items" : [ ]
        }
      } ],
      "displayName" : "Sqoop 1 Client"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "7db0df38-5dd4-4a05-9fef-d6bbc6b261ef",
    "ipAddress" : "172.31.16.190",
    "hostname" : "ip-172-31-16-190.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "b92816dd-e84a-45e6-b718-28f05bc745b0",
    "ipAddress" : "172.31.16.27",
    "hostname" : "ip-172-31-16-27.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "2a0a0720-5d03-47a8-af3e-0cebf21d50f0",
    "ipAddress" : "172.31.23.194",
    "hostname" : "ip-172-31-23-194.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4",
    "ipAddress" : "172.31.26.85",
    "hostname" : "ip-172-31-26-85.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "beb05496-6801-4d54-8ae8-8858655e00fa",
    "ipAddress" : "172.31.27.141",
    "hostname" : "ip-172-31-27-141.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__0d18cef1-48eb-4dd3-a3b0-8193e03428a3",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "9a774fb123432b0a06ccd545c8ec7dfe20cdb690bc4da06258740551223219e8",
    "pwSalt" : -1699594595738507101,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-2c31286b24af8b05a30991e52dfb7dfb",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "6692e957cd2b1236fda2c22b5764fbf394258b94c9a745173738189faee28d10",
    "pwSalt" : 3600580394247246143,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-2c31286b24af8b05a30991e52dfb7dfb",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "6616d1ee363997b84b4bf9c8b412201ac4669d98783816e5064213c2c7470122",
    "pwSalt" : 4017045332951487157,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-2c31286b24af8b05a30991e52dfb7dfb",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "cb80837081afe757cecea578852f7a7a02cd9e06ffe2b4380b532b50aea6a4ce",
    "pwSalt" : -6158900919796292974,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-2c31286b24af8b05a30991e52dfb7dfb",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "2472131c4a259262a75d231e597856e2af0f5226ff6549eb678f50dcce13ca11",
    "pwSalt" : 4794484171633408305,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-2c31286b24af8b05a30991e52dfb7dfb",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "29e38e5d88a81d9493b7809c7d544f5475fbfce03db8bb912cbce77afb8ab6d2",
    "pwSalt" : -7681119490387369322,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "9d16d8d93162bba5644cf85f7aa1ef7394872563b9ff6186eb9b3f128aea926e",
    "pwSalt" : -5738426518722525135,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "b0e42d6ae7f6cf1f843fae71e6b6659670eef70d28c315bcf1459a8d1eb4cd1e",
    "pwSalt" : 2488984149081261500,
    "pwLogin" : true
  }, {
    "name" : "tantalus1984",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "707ee18feeae6c17a78bc9042f4f264f9faf72ce0b57ecbd34bff50044779c03",
    "pwSalt" : -4260858841365023151,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20161019-1014",
    "gitHash" : "518f0d6d44abc87bc392646e4369a20c8192b7cf",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "ip-172-31-26-85.eu-central-1.compute.internal"
        }, {
          "name" : "firehose_database_name",
          "value" : "amon"
        }, {
          "name" : "firehose_database_password",
          "value" : "amon_password"
        }, {
          "name" : "firehose_database_user",
          "value" : "amon"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-26-85.eu-central-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman_password"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-2c31286b24af8b05a30991e52dfb7dfb",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7di1sxuynq5kqezzecvai75gv"
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-2c31286b24af8b05a30991e52dfb7dfb",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2b6u9yhx8gmf4ysqu0lgcri4b"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-2c31286b24af8b05a30991e52dfb7dfb",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "793thq5u6uaxvaiyxpqprmoy9"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-2c31286b24af8b05a30991e52dfb7dfb",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2zfn1gftu3lw4vcwzxnmtg7he"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-2c31286b24af8b05a30991e52dfb7dfb",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6nqlswoxh00f3rql1t3fep4qn"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-2c31286b24af8b05a30991e52dfb7dfb",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "591ebf5d-dcc8-4998-94ca-18f804c758e4"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "cv88l0dw68txayofwdmg6nda0"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "AGENT_TLS",
      "value" : "true"
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/25/2012 17:10"
    }, {
      "name" : "KEYSTORE_PASSWORD",
      "value" : "password"
    }, {
      "name" : "KEYSTORE_PATH",
      "value" : "/opt/cloudera/security/pki/ip-172-31-26-85.eu-central-1.compute.internal-server.jks"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://ec2-54-93-77-231.eu-central-1.compute.amazonaws.com/cdh5.8.3/,http://ec2-54-93-77-231.eu-central-1.compute.amazonaws.com/cdh5.9.1,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    }, {
      "name" : "WEB_TLS",
      "value" : "true"
    } ]
  }
}
```
