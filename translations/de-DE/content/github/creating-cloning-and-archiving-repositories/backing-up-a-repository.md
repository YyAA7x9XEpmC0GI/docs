---
title: Sicherung eines Repositorys durchführen
intro: 'Du kannst{% if enterpriseServerVersions contains currentVersion or currentVersion == "github-ae@latest" %} Git und{% endif %} die API {% if currentVersion == "free-pro-team@latest" %}oder ein Drittanbieter-Werkzeug {% endif %}für die Sicherung Deines Repositorys verwenden.'
redirect_from:
  - /articles/backing-up-a-repository
versions:
  free-pro-team: '*'
  enterprise-server: '*'
  github-ae: '*'
topics:
  - Repositories
---

{% if currentVersion == "free-pro-team@latest" %}

Um ein Archiv Deines Repositorys herunterzuladen, kannst du die API für die Migration von Benutzern oder Organisationen verwenden. For more information, see "[Migrations](/rest/reference/migrations)."
{% else %}

Du kannst Deine Repositorys manuell herunterladen und sichern:

- Um die Git-Daten eines Repositorys auf Deinen lokalen Computer herunterzuladen, musst Du das Repository klonen. Weitere Informationen findest Du unter „[Ein Repository clonen](/articles/cloning-a-repository)“.
- Du kannst auch das Wiki Deines Repositorys herunterladen. Weitere Informationen findest Du unter „[Wiki-Seiten hinzufügen oder bearbeiten](/communities/documenting-your-project-with-wikis/adding-or-editing-wiki-pages).“

Wenn Du ein Repository oder Wiki klonst, werden nur Git-Daten wie Projektdateien und der Commit-Verlauf heruntergeladen. Mithilfe unserer API kannst Du andere Elemente Deines {% data variables.product.product_name %}-Repositorys auf Deinen lokalen Computer herunterladen:

- [Issues](/rest/reference/issues#list-issues-for-a-repository)
- [Pull Requests](/rest/reference/pulls#list-pull-requests)
- [Forks](/rest/reference/repos#list-forks)
- [Kommentare](/rest/reference/issues#list-issue-comments-for-a-repository)
- [Meilensteine](/rest/reference/issues#list-milestones)
- [Kennzeichnungen](/rest/reference/issues#list-labels-for-a-repository)
- [Watcher](/rest/reference/activity#list-watchers)
- [Stargazers](/rest/reference/activity#list-stargazers)
- [Projekte](/rest/reference/projects#list-repository-projects)
{% endif %}

Sobald Sie {% if enterpriseServerVersions contains currentVersion or currentVersion == "github-ae@latest" %}eine lokale Version aller Inhalte haben, die Sie sichern möchten, können Sie ein ZIP-Archiv erstellen und {% else %}Ihr Archiv heruntergeladen haben, können Sie {% endif %}es auf eine externe Festplatte kopieren und/oder auf einen Cloud-basierten Dienst wie [Google Drive](https://www.google.com/drive/) oder [Dropbox](https://www.dropbox.com/) hochladen.

{% if currentVersion == "free-pro-team@latest" %}
### Backup-Tools (Sicherungswerkzeuge) von Drittanbietern
Es sind mehrere Self-Service-Tools verfügbar, mit denen Du die Sicherung von Repositorys automatisieren kannst. Unlike archival projects, which archive _all_ public repositories on

{% data variables.product.product_name %} that have not opted out and make the data accessible to anyone, backup tools will download data from _specific_ repositories and organize it within a new branch or directory. Weitere Informationen zu Archivierungsprojekten findest Du unter „[Über die Archivierung von Inhalt und Daten auf {% data variables.product.prodname_dotcom %}](/github/creating-cloning-and-archiving-repositories/about-archiving-content-and-data-on-github#about-the-github-archive-program)." For more information about self-service backup tools, see the [Backup Utilities category on {% data variables.product.prodname_marketplace %}](https://github.com/marketplace?category=backup-utilities).
{% endif %}
