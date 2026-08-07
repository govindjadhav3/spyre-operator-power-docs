# Secondary Scheduler Operator

<!-- Last Updated: 2026-01-22 -->

The Secondary Scheduler Operator allows you to deploy a custom scheduler alongside the default Red Hat OpenShift scheduler.

To install the Secondary Scheduler Operator for Red Hat OpenShift, use the web console.

## Procedure

1. Log in to the Red Hat OpenShift web console.
2. Create the required namespace for the Secondary Scheduler Operator for Red Hat OpenShift:
   - Navigate to **Administration > Namespaces** and click **Create Namespace**.
   - Enter `openshift-secondary-scheduler-operator` in the **Name** field and click **Create**.
3. Install the Secondary Scheduler Operator for Red Hat OpenShift:
   - Navigate to **Operators > OperatorHub**.
   - Enter **Secondary Scheduler Operator for Red Hat OpenShift** into the filter box.
   - Select the **Secondary Scheduler Operator for Red Hat OpenShift** and click **Install**.
   - On the **Install Operator** page, configure the following settings:
     - **Update channel**: set to **stable**, which installs the latest stable release.
     - **Installed Namespace**: select **A specific namespace on the cluster** and select `openshift-secondary-scheduler-operator` from the drop-down menu.
     - **Update approval**: select **Automatic** to allow OLM to update the Operator automatically, or **Manual** to require approval.
   - Click **Install**.
4. Navigate to **Operators > Installed Operators**.
5. Verify that the **Secondary Scheduler Operator for Red Hat OpenShift** is listed with a **Status** of **Succeeded**.

**Note:** You *may* need to create the appropriate namespace for the secondary scheduler operator installation. If the namespace `openshift-secondary-scheduler-operator` is not present, you will have to create the namespace with the following command before the installation:

```bash
oc create namespace openshift-secondary-scheduler-operator
```

## Parent topic:

[Prerequisites on Red Hat OpenShift using OperatorHub](prerequisites.md)
