---
title: Manage projects
enableTableOfContents: true
isDraft: false
redirectFrom:
  - /docs/get-started-with-neon/projects
---

A project is the top-level object in the Neon object hierarchy. Tier limits define how many projects you can create. Neon's free tier permits one project per Neon account.

A Neon project is created with the following resources by default:

- A root branch called `main`. You can create child branches from the root branch or from a previously created branch. For more information, see [Branches](../branches).
- A single read-write endpoint. An endpoint is the compute instance associated with a branch. For more information, see [Endpoints](../branches).
- A default database, called `neondb`, which resides in the project's root branch.
- A default PostgreSQL user that takes its name from your Neon account (the Google, GitHub, or partner account that you registered with).
- A `web_access` PostgreSQL user, which is used by the Neon [SQL Editor](../../get-started-with-neon/query-with-neon-sql-editor) and for [passwordless connections](../../connect/passwordless-connect).

## Create a project

To create a Neon project:

1. Navigate to the [Neon Console](https://console.neon.tech).
2. If you are creating your very first project, click **Create your first project**. Otherwise, click **New Project**.
3. Specify a name, a PostgreSQL version, a region, and click **Create Project**.

Upon creating a project, you are presented with a dialog that provides your connection details for the project, including your password. The password is required to connect to databases in the project from a client or application. Store your password in a safe location.

<Admonition type="important">
After closing the connection information dialog, your password is no longer accessible. If you forget or misplace your password, your only option is to reset it. For password reset instructions, see [Users](../users).
</Admonition>

## Edit a project

Only changing the project name and enabling or disabling connection pooling are permitted when editing a project.

To edit a Neon project:

1. Navigate to the [Neon Console](https://console.neon.tech).
2. Select the project that you want to edit.
3. Select **Settings** > **General**.
4. Make your changes and click **Save**.

## Delete a project

Deleting a project is a permanent action, which also deletes any endpoints, branches, databases, and users that belong to the project.

To delete a project:

1. Navigate to the [Neon Console](https://console.neon.tech).
2. Select the project that you want to delete.
3. Select **Settings** > **General**.
4. Click **Delete project.**
5. On the confirmation dialog, click **Delete**.

## Need help?

Send a request to [support@neon.tech](mailto:support@neon.tech), or join the [Neon community forum](https://community.neon.tech/).
