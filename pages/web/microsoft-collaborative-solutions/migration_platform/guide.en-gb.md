---
title: "Migrating your email addresses from one OVHcloud email platform to another"
slug: migration-email-platform
excerpt: "Find out how to migrate email addresses from one Exchange or Email Pro platform to another Exchange, Email Pro or MX Plan platform"
section: Account migration
order: 2
---

**Last updated 21/10/2020**

## Objective

You want to migrate your email addresses on an Exchange or Email Pro platform to another Exchange, Email Pro or MX Plan platform. In this guide, you will find a two-phase migration process:

1. **Configure the destination** platform.
2. **Migrate email** accounts from your current platform to the new one.

![email-migration](images/migration_platform01.gif){.thumbnail}

> [!primary]
>
> To migrate an MX Plan solution to an Exchange or Email Pro platform, please follow our guide on [Migrating an MX Plan email address to an Email Pro or Exchange](https://docs.ovh.com/gb/en/microsoft-collaborative-solutions/migration-email-address-to-exchange/) account.
>

**Find out how to migrate email addresses from one Exchange or Email Pro platform to another Exchange or Email Pro platform.**

## Requirements

- a **“source”** platform with configured [Exchange](https://www.ovh.co.uk/emails/hosted-exchange/){.external} or [Email Pro](https://www.ovh.co.uk/emails/email-pro/){.external} accounts
- a **“destination”** platform with [Exchange](https://www.ovh.co.uk/emails/hosted-exchange/){.external}, [Email Pro](https://www.ovh.co.uk/emails/email-pro/){.external} or MX Plan accounts (via the MX Plan solution or included in [OVHcloud web hosting plans](https://www.ovh.co.uk/web-hosting/){.external}) This platform must have accounts that are not configured or available to host the email addresses that need to be migrated.
- access to the [OVHcloud Control Panel](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.co.uk/&ovhSubsidiary=GB){.external}

## Instructions

### Configure the destination platform

Before you begin your migration, if you have just ordered your new email solution, first add the domain name to your [Email Pro](https://docs.ovh.com/gb/en/emails-pro/first-configuration-email-pro/#step-2-add-your-domain-name) or [Exchange](https://docs.ovh.com/gb/en/microsoft-collaborative-solutions/adding-domain-exchange/) platform. If you are migrating to an MX Plan platform, with the domain name attached as “fixed”, you can proceed directly to [the next step](#accountsmigration) .

> Select the `Associated`{.action} domains tab for your platform, then click `Add a domain`{.action}. Configure your domain name as **non-authoritative**. Once you have added your domain name, ensure that the word `OK` appears in the `Status` column.
>
> ![email-migration](images/migration_platform02.png){.thumbnail}
>
> For more details on adding a domain name, follow [the Email Pro](https://docs.ovh.com/gb/en/emails-pro/first-configuration-email-pro/#step-2-add-your-domain-name) guide or [the Exchange](https://docs.ovh.com/gb/en/microsoft-collaborative-solutions/adding-domain-exchange/) guide.

### Migrate email accounts <a name="accountsmigration"></a>

Your email accounts will be migrated in 3 main steps: **Rename** the original email account, **create** the new email account and **migrate** from the original platform to the new one.

![email-migration](images/migration_platform03.gif){.thumbnail}

> [!warning]
>
> Special case:
>
> - If you need to migrate **an Exchange** account to an **Email Pro** account, you must ensure that your email accounts do not exceed 10 GB. Collaborative features, calendar and contact synchronisation are not present on Email Pro and cannot be migrated.
> - If you need to migrate **an Exchange or Email Pro** account to an **MX Plan** account, you must ensure that your email account does not exceed 5 GB. Collaborative features, calendar and contact synchronisation are not present on MX Plan and cannot be migrated.

#### Rename

Rename the email account to be migrated with a provisional name (e.g.: to migrate the email account *john.smith@mydomain.ovh*, rename it to *john.smith01@mydomain.ovh*).

In the `Email`{.action} accounts tab for your email platform, click the `...`{.action} button, then `Modify`{.action}.

![email-migration](images/migration_platform04.png){.thumbnail}

#### Create

Create your email address on the new account for your Email Pro, Exchange or MX Plan platform (using the previous example, you will create *john.smith@mydomain.ovh* on your new platform)

In the `Email`{.action} accounts tab for your platform, click the `...`{.action} button, to the right of the target email account, then `Modify`{.action}.

![email-migration](images/migration_platform05.png){.thumbnail}

#### Migrer

Migrate the source email account to your new platform's account using our [OMM](https://omm.ovh.net/) tool (OVH Mail Migrator).

For more information on OMM, please read our guide on [Migrating email accounts via the OVH Mail Migrator](https://docs.ovh.com/gb/en/microsoft-collaborative-solutions/exchange-account-migration-with-ovh-mail-migrator/).

![email-migration](images/migration_platform06.png){.thumbnail}

The migration time depends on the amount of data to migrate to your new account. This may vary from a few minutes to several hours.

Check after the migration that you can find all of your elements by logging into webmail at <https://www.ovh.co.uk/mail/>.

Once the migration is complete, you can keep or delete the original account with the temporary name.

If you would like to delete it, go to the Email `accounts`{.action} tab on your original email platform, click on the `...`{.action} button, then `Reset this account`{.action}.

### Check or modify your domain configuration

At this stage, your email addresses must already be migrated and functional. For security reasons, please ensure that your domain is correctly configured in your Control Panel.

To do this, select the Email Pro or Exchange service concerned in the services bar on the left-hand side, then go to the `Associated`{.action} domains tab. In the table shown, you can use the Diagnostic column to check if the DNS configuration is correct: a red box appears if the configuration needs to be modified.

> [!primary]
>
> If you have just migrated or modified a DNS record for your domain, it may take a few hours to be updated when you go to the [OVHcloud Control Panel](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.co.uk/&ovhSubsidiary=GB){.external}.
>

To modify the configuration, click on the red box and carry out the requested operation. It can take between 4 and a maximum of 24 hours to propagate fully.

![email-migration](images/check_the_dns_records_associated_domains.png){.thumbnail}

### Use your migrated email addresses

Now, you can start using your migrated email addresses. To do this, OVHcloud offers an online application (_web app_), available here <https://www.ovh.co.uk/mail/>. You will need to enter your email credentials.

If you have configured one of the migrated accounts on an email client (example: Outlook, Thunderbird), you will need to configure it again. The login details for the OVHcloud server have changed following the migration.
<br>To help you make changes, please read our guide via the [Email Pro](https://docs.ovh.com/gb/en/emails-pro/){.external} and [Hosted Exchange](https://docs.ovh.com/gb/en/microsoft-collaborative-solutions/){.external} guide sections. If you are unable to reconfigure the account immediately, access via the online application is always possible.

> [!primary]
>
> You can also manually migrate email addresses to OVHcloud by using our [OVH Mail Migrator (OMM)](https://omm.ovh.net/){.external} tool. To do this, you must have the information (user, password, servers) of the source email and the destination email.
>

## Go further

[Managing contacts for your services](https://docs.ovh.com/gb/en/customer/managing-contacts/){.external}

[Email Pro guides](https://docs.ovh.com/gb/en/emails-pro/){.external}

[Exchange guides](https://docs.ovh.com/gb/en/microsoft-collaborative-solutions/){.external} 

Join our community of users on <https://community.ovh.com/en/>