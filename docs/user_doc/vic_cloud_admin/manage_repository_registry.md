# Manage Internal Repositories in Projects

You can access the list of internal repositories that users have pushed to a project. You can browse repositories to see the different tags applied to images in the repository. You can also delete a repository or a tag in a repository.

Deleting a repository involves two steps. First, you delete a repository in vSphere Integrated Containers Management Portal. This is known as soft deletion. You can delete the entire repository or just one tag in the repository. After a soft deletion, the registry no longer manages the repository. However, the repository files remain in the registry storage until you run garbage collection by restarting the registry.

**Prerequisites**

You have created a project and pushed at least one repository to the project.

**Procedure**

1. In the management portal, navigate to **Administration** > **Projects** > **Your_project**.
   
    Use an account with the Cloud Administrator role, or an account that has the DevOps Admin role for this project.

2. Click the **Internal Repositories** tab to see the number of tags that the repository contains and how many times that users have pulled the repository
3. (Optional) To delete a repository, select the check box next to a repository name and click **Delete**.

   **CAUTION**: If two tags refer to the same image, if you delete one tag, the other tag is also deleted.
4. Click a repository name to view its contents.

**What to Do Next**

If you deleted respositories, and if the registry is configured with garbage collection enabled, restart the registry. vSphere Integrated Containers Registry will perform garbage collection when it reboots. For information about restarting the registry, see [Restart the vSphere Integrated Containers Services](../vic_vsphere_admin/restart_services.md) in *Install, Deploy, and Maintain the vSphere Integrated Containers Infrastructure*.