# Terms of Service

_Last updated: 2026-05-12_

These terms govern use of **myOnlineBanking** ("the App") by its owner. The App is a strictly private, self-hosted banking aggregator that displays accounts and transactions from the owner's own bank accounts via the Enable Banking PSD2 API. It is **not** offered, licensed, or supported for use by any other person.

By installing, running, or using the App, the owner agrees to these terms.

## 1. What the App is — and isn't

- The App is a **strictly private finance viewer for its owner's own accounts**. It reads account information from banks the owner explicitly connects and to which the owner is the legitimate account holder. It does **not** initiate payments, transfers, or any other financial operation.
- The App is **self-hosted software** run by the owner on the owner's own hardware. There is no hosted service, no uptime guarantee, no managed instance, and no customer support entitlements.
- The App is **not affiliated** with Enable Banking Oy, with any bank, or with any payment institution. References to those parties are descriptive only.

## 2. Scope of permitted use

- The App may be used **only by its owner**, and **only to access bank accounts of which the owner is the legitimate account holder**. Accessing another person's accounts — even with that person's consent — is outside the permitted scope.
- The App is for **strictly personal, non-commercial, private use** in the sense of GDPR Article 2(2)(c) (the household exemption). Using it on behalf of others, in a professional capacity, as part of an employer's infrastructure, or as a service of any kind is prohibited.
- The owner must be of full legal age in their jurisdiction.

## 3. The owner's responsibilities

The owner is responsible for:

- registering and maintaining their own application with Enable Banking, including holding the corresponding private key securely;
- complying with [Enable Banking's terms](https://enablebanking.com/terms/) and with the terms of every bank connected;
- the security of the machine on which the App runs (operating system, disk encryption, network exposure);
- any costs that arise from use of the Enable Banking API, including the consequences of moving from the free restricted-production tier to a paid plan;
- backing up or deleting data stored locally by the App;
- ensuring that no other person is given access to the running App, the database file, or the private key.

## 4. Disclaimer of warranty

THE APP IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, ACCURACY, AVAILABILITY, AND NON-INFRINGEMENT.

In particular:

- Balances and transactions are read from upstream sources and may be **delayed, incomplete, or incorrect**. The App must not be used as the sole source of truth for any financial decision.
- The App may at any time fail to display data because of changes at the owner's bank, at Enable Banking, in the PSD2 regulatory regime, or in the App itself.

## 5. Limitation of liability

To the maximum extent permitted by applicable law, in no event shall the author of the App be liable for any direct, indirect, incidental, special, consequential, or exemplary damages — including but not limited to loss of funds, missed payments, overdraft fees, lost data, or reputational harm — arising from the owner's use of, or inability to use, the App.

Because the App is operated by the owner for their own private benefit, any loss resulting from its use is borne by the owner alone. If liability cannot be excluded under applicable law, it is limited to the amount the owner paid for the App. The App is distributed free of charge, so this amount is zero.

## 6. Third-party services

Connecting a bank involves interactions with at least two third parties:

- **Enable Banking Oy**, which provides the API and the consent flow. Your use of Enable Banking is governed by its own terms and privacy policy.
- **Your banks**, each of which has its own terms governing access to your account data over PSD2.

The author of the App is not a party to those agreements and cannot enforce or override them on your behalf.

## 7. Data and privacy

How the App handles data is described in the [Privacy Policy](./PRIVACY.md). In short: the App stores only minimal session metadata locally, fetches account and transaction data live from Enable Banking, and shares it with no other parties.

## 8. Intellectual property and licence

The source code of the App is owned by [YOUR NAME] and is made available under [LICENCE — e.g. MIT, AGPL-3.0]. Use of the App outside the scope of that licence is not permitted. Logos and trademarks belonging to banks or to Enable Banking remain the property of their respective owners.

## 9. Changes to the App and to these terms

The App may be updated, changed, or discontinued at any time. These terms may also be updated; the revised version takes effect when committed to the project repository, and the "Last updated" date at the top will be revised accordingly. Continued use of the App after a change constitutes acceptance of the new terms.

## 10. Termination

You may stop using the App at any time by uninstalling it and deleting the `data/` directory. Sections 4, 5, 7, and 8 survive termination.

## 11. Governing law

These terms are governed by the laws of [YOUR JURISDICTION], without regard to its conflict-of-laws rules. Any dispute will be brought before the competent courts of [YOUR JURISDICTION].

## 12. Contact

For questions about these terms, contact [YOUR EMAIL].
