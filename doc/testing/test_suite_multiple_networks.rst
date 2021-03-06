=================
Multiple Networks
=================


Contrail HA Multiple Networks
-----------------------------


ID
##

contrail_ha_multiple_networks


Description
###########

Deploy Contrail HA environment with Neutron GRE and 2 nodegroups


Complexity
##########

advanced


Steps
#####

    1. Revert snapshot with ready master node
    2. Install contrail plugin
    3. Enable dedicated analytics DB
    4. Bootstrap slaves from default nodegroup
    5. Create cluster with Neutron GRE and custom nodegroups
    6. Activate plugin and configure plugins setings
    7. Remove 2nd custom nodegroup which is added automatically
    8. Bootstrap slave nodes from custom nodegroup
    9. Download network configuration
    10. Update network.json  with customized ip ranges
    11. Put new json on master node and update network data
    12. Verify that new IP ranges are applied for network config
    13. Add following nodes to default nodegroup:
        * 3 controller+ceph
    14. Add following nodes to custom nodegroup:
        * 1 compute
        * 1 contrail-config+contrail-control+contrail-db+
          contrail-analytics+contrail-analytics-db
        * 1 contrail-analytics+contrail-analytics-db
    15. Deploy cluster
    16. Run network verification
    17. Verify that excluded ip is not used for nodes or VIP
    18. Run health checks (OSTF)

Expected results
################
All steps must be completed successfully, without any errors


Contrail Multiple Networks delete controller
--------------------------------------------


ID
##

contrail_multiple_networks_delete_controller


Description
###########

Check Contrail deploy multiple networks remove controller


Complexity
##########

advanced


Steps
#####

    1. Revert snapshot with ready master node
    2. Install contrail plugin
    3. Bootstrap slaves from default nodegroup
    4. Create cluster with Neutron GRE and custom nodegroups
    5. Activate plugin and configure plugins setings
    6. Remove 2nd custom nodegroup which is added automatically
    7. Bootstrap slave nodes from custom nodegroup
    8. Download network configuration
    9. Update network.json  with customized ip ranges
    10. Put new json on master node and update network data
    11. Verify that new IP ranges are applied for network config
    12. Add following nodes to default nodegroup:
        * 1 controller+cinder
        * 2 controller
    13. Add following nodes to custom nodegroup:
        * 1 compute
        * 1 contrail-config+contrail-control+contrail-db
        * 1 contrail-analytics
    14. Deploy cluster
    15. Run health checks (OSTF)
    16. Remove 1 controller node
    17. Redeploy cluster
    18. Run health checks (OSTF)


Expected results
################
All steps must be completed successfully, without any errors


Contrail Multiple Networks add controller
-----------------------------------------


ID
##

contrail_multiple_networks_add_controller


Description
###########

Check Contrail deploy multiple networks add controller


Complexity
##########

advanced


Steps
#####

    1. Revert snapshot with ready master node
    2. Install contrail plugin
    3. Enable dedicated analytics DB
    4. Bootstrap slaves from default nodegroup
    5. Create cluster with Neutron GRE and custom nodegroups
    6. Activate plugin and configure plugins setings
    7. Remove 2nd custom nodegroup which is added automatically
    8. Bootstrap slave nodes from custom nodegroup
    9. Download network configuration
    10. Update network.json  with customized ip ranges
    11. Put new json on master node and update network data
    12. Verify that new IP ranges are applied for network config
    13. Add following nodes to custom nodegroup:
        * 1 controller+mongo
    14. Add following nodes to default nodegroup:
        * 1 compute
        * 1 contrail-config+contrail-control+contrail-db+
          contrail-analytics
        * 1 contrail-analytics-db
        * 1 cinder
    15. Deploy cluster
    16. Run health checks (OSTF)
    17. Add 1 controller node
    18. Redeploy cluster
    19. Run health checks (OSTF)


Expected results
################
All steps must be completed successfully, without any errors


Contrail Multiple Networks delete compute
-----------------------------------------


ID
##

contrail_multiple_networks_delete_compute


Description
###########

Check Contrail deploy multiple networks remove compute


Complexity
##########

advanced


Steps
#####

    1. Revert snapshot with ready master node
    2. Install contrail plugin
    3. Bootstrap slaves from default nodegroup
    4. Create cluster with Neutron GRE and custom nodegroups
    5. Activate plugin and configure plugins setings
    6. Remove 2nd custom nodegroup which is added automatically
    7. Bootstrap slave nodes from custom nodegroup
    8. Download network configuration
    9. Update network.json  with customized ip ranges
    10. Put new json on master node and update network data
    11. Verify that new IP ranges are applied for network config
    12. Add following nodes to default nodegroup:
        * 3 controller
    13. Add following nodes to custom nodegroup:
        * 2 compute
        * 1 contrail-config+contrail-control+contrail-db+contrail-analytics
    14. Deploy cluster
    15. Run health checks (OSTF)
    16. Remove 1 compute node
    17. Redeploy cluster
    18. Run health checks (OSTF)


Expected results
################

All steps must be completed successfully, without any errors


Contrail Multiple Networks add compute
--------------------------------------

ID
##

contrail_multiple_networks_add_compute


Description
###########

Check Contrail deploy multiple networks add compute


Complexity
##########

advanced


Steps
#####

    1. Revert snapshot with ready master node
    2. Install contrail plugin
    3. Enable dedicated analytics DB
    4. Bootstrap slaves from default nodegroup
    5. Create cluster with Neutron GRE and custom nodegroups
    6. Activate plugin and configure plugins setings
    7. Remove 2nd custom nodegroup which is added automatically
    8. Bootstrap slave nodes from custom nodegroup
    9. Download network configuration
    10. Update network.json  with customized ip ranges
    11. Put new json on master node and update network data
    12. Verify that new IP ranges are applied for network config
    13. Add following nodes to default nodegroup:
        * 3 controller
    14. Add following nodes to custom nodegroup:
        * 1 compute+ceph-osd
        * 1 contrail-config+contrail-control+contrail-db+
          contrail-analytics
        * 1 contrail-analytics-db
    15. Deploy cluster
    16. Run health checks (OSTF)
    17. Add 1 compute node
    18. Redeploy cluster
    19. Run health checks (OSTF)


Expected results
################
All steps must be completed successfully, without any errors


Contrail Multiple Networks contrail HA
--------------------------------------

ID
##

contrail_different_ha_in_multinet


Description
###########

Check Contrail deploy multiple networks with contrail HA


Complexity
##########

advanced


Steps
#####

    1. Revert snapshot with ready master node
    2. Install contrail plugin
    3. Enable dedicated analytics DB
    4. Bootstrap slaves from default nodegroup
    5. Create cluster with Neutron GRE and custom nodegroups
    6. Activate plugin and configure plugins setings
    7. Remove 2nd custom nodegroup which is added automatically
    8. Bootstrap slave nodes from custom nodegroup
    9. Download network configuration
    10. Update network.json  with customized ip ranges
    11. Put new json on master node and update network data
    12. Verify that new IP ranges are applied for network config
    13. Add following nodes to default nodegroup:
        * 1 controller
        * 2 contrail-config+contrail-control+contrail-db+
          contrail-analytics
    14. Add following nodes to custom nodegroup:
        * 1 cinder
        * 1 contrail-config+contrail-control+contrail-db+
          contrail-analytics
        * 1 contrail-analytics-db
    15. Deploy cluster
    16. Run health checks (OSTF)

Expected results
################
All steps must be completed successfully, without any errors