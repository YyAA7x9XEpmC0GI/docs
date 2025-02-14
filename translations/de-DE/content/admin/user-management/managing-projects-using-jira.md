---
title: Managing projects using Jira
intro: 'You can integrate Jira with {% data variables.product.prodname_enterprise %} for project management.'
redirect_from:
  - /enterprise/admin/guides/installation/project-management-using-jira/
  - /enterprise/admin/articles/project-management-using-jira/
  - /enterprise/admin/developer-workflow/managing-projects-using-jira
  - /enterprise/admin/developer-workflow/customizing-your-instance-with-integrations
  - /enterprise/admin/user-management/managing-projects-using-jira
versions:
  enterprise-server: '*'
type: how_to
topics:
  - Enterprise
  - Project management
---

### Connecting Jira to a {% data variables.product.prodname_enterprise %} organization

1. Melden Sie sich unter „http[s]://[hostname]/login“ bei Ihrem {% data variables.product.prodname_enterprise %}-Konto an. If already signed in, click on the {% data variables.product.prodname_dotcom %} logo in the top left corner.
2. Click on your profile icon under the {% data variables.product.prodname_dotcom %} logo and select the organization you would like to connect with Jira.

  ![Select an organization](/assets/images/enterprise/orgs-and-teams/profile-select-organization.png)

3. Click on the **Edit _organization name_ settings** link.

  ![Edit organization settings](/assets/images/enterprise/orgs-and-teams/edit-organization-settings.png)

4. In the left sidebar, under **Developer settings**, click **OAuth Apps**.

  ![Select OAuth Apps](/assets/images/enterprise/orgs-and-teams/organization-dev-settings-oauth-apps.png)

5. Click on the **Register new application** button.

  ![Register new application button](/assets/images/enterprise/orgs-and-teams/register-oauth-application-button.png)

6. Tragen Sie die Anwendungseinstellungen ein:
    - In the **Application name** field, type "Jira" or any name you would like to use to identify the Jira instance.
    - In the **Homepage URL** field, type the full URL of your Jira instance.
    - In the **Authorization callback URL** field, type the full URL of your Jira instance.
7. Klicke auf **Register application** (Anwendung registrieren).
8. Beachten Sie oben auf der Seite die **Client-ID** und das **Clientgeheimnis**. You will need these for configuring your Jira instance.

### Jira instance configuration

1. On your Jira instance, log into an account with administrative access.
2. At the top of the page, click the settings (gear) icon and choose **Applications**.

  ![Select Applications on Jira settings](/assets/images/enterprise/orgs-and-teams/jira/jira-applications.png)

3. In the left sidebar, under **Integrations**, click **DVCS accounts**.

  ![Jira Integrations menu - DVCS accounts](/assets/images/enterprise/orgs-and-teams/jira/jira-integrations-dvcs.png)

4. Click **Link Bitbucket Cloud or {% data variables.product.prodname_dotcom %} account**.

  ![Link GitHub account to Jira](/assets/images/enterprise/orgs-and-teams/jira/jira-link-github-account.png)

5. Tragen Sie im Modalfenster **Add New Account** (Neues Konto hinzufügen) Ihre {% data variables.product.prodname_enterprise %}-Einstellungen ein:
    - From the **Host** dropdown menu, choose **{% data variables.product.prodname_enterprise %}**.
    - Geben Sie im Feld **Team or User Account** den Namen Ihrer {% data variables.product.prodname_enterprise %}-Organisation oder Ihres persönlichen Kontos ein.
    - Geben Sie im Feld **OAuth Key** (OAuth-Schlüssel) die Client-ID Ihrer {% data variables.product.prodname_enterprise %}-Entwickleranwendung ein.
    - Geben Sie im Feld **OAuth Secret** (OAuth-Geheimnis) das Clientgeheimnis für Ihre {% data variables.product.prodname_enterprise %}-Entwickleranwendung ein.
    - If you don't want to link new repositories owned by your {% data variables.product.prodname_enterprise %} organization or personal account, deselect **Auto Link New Repositories**.
    - If you don't want to enable smart commits, deselect **Enable Smart Commits**.
    - Klicke auf **Add** (Hinzufügen).
6. Überprüfen Sie die Berechtigungen, die Sie Ihrem {% data variables.product.prodname_enterprise %}-Konto erteilen, und klicken Sie auf **Authorize application** (Anwendung autorisieren).
7. Geben Sie zum Fortfahren ggf. Ihr Passwort ein.
