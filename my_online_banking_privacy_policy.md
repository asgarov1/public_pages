# Privacy Policy

_Last updated: 2026-05-12_

This privacy policy explains how **myOnlineBanking** ("the App") handles personal and financial data. The App is a strictly private, self-hosted aggregator: it is operated by a single person — the owner — exclusively to view that owner's own bank accounts and transactions on a single overview page. It is not offered to any other natural or legal person, and it never processes data belonging to anyone other than the owner.

The owner (acting simultaneously as data controller and as the sole data subject) is:

- **Name:** Javid Asgarov
- **Address:** Tulbingerkogel
- **Email:** asgarov1@gmail.com

Because the owner is the only person who uses the App and the only person whose data is processed by it, this policy is in practice a self-imposed description of how the software behaves with that single person's data.

## 1. Scope

The App is used **only** for the owner's private financial overview. It must not be used to access, store, display, or otherwise process the personal or financial data of any other individual. Where this policy refers to "you", it refers to the owner alone; no other data subject is contemplated.

## 2. What data is processed

The App processes the following categories of the owner's personal data:

| Category                 | Examples                                                                                                  | Source                          |
| ------------------------ | --------------------------------------------------------------------------------------------------------- | ------------------------------- |
| Bank account metadata    | IBAN, BBAN, masked PAN, account name, product, currency, bank name, country                               | Your bank, via Enable Banking   |
| Balances                 | Booked / available balance, currency, reference date                                                      | Your bank, via Enable Banking   |
| Transactions             | Booking date, value date, amount, currency, counterparty (creditor/debtor name), remittance, status       | Your bank, via Enable Banking   |
| Authentication artefacts | Enable Banking session identifier, consent validity timestamps                                            | Enable Banking                  |
| Technical data           | Application logs (timestamps, error messages, ASPSP names)                                                | The App itself                  |

The App does **not** collect biometric data, location data, marketing identifiers, advertising IDs, or any third-party analytics data.

## 3. What is stored locally vs. fetched live

- **Stored locally** (in the H2 database file under `./data/`): the Enable Banking session identifier, the ASPSP name and country code, the time the bank was connected, and the consent's "valid until" timestamp. No balances, no transactions, and no account numbers are persisted by default.
- **Fetched live** on every page load: account list, balances, and transactions. These are held in memory only and discarded when the response is rendered.
- **Stored as files on disk**: the RSA private key used to sign API requests to Enable Banking (`secrets/`), and standard application logs.

## 4. Lawful basis for processing (GDPR)

Processing is carried out on the basis of:

- **Article 6(1)(a) — consent**: the owner grants consent for each bank during the PSD2 Strong Customer Authentication flow at the bank's website.
- **Household exemption (Article 2(2)(c))**: because the App is used by a single natural person in the course of a purely personal activity (managing their own finances), the GDPR's substantive obligations arguably do not apply at all. This policy is provided as a matter of transparency rather than as an admission that the GDPR is engaged.

## 5. Recipients and processors

The App relies on the following third party to access bank data:

- **Enable Banking Oy** (Helsinki, Finland) — a regulated Account Information Service Provider (AISP) authorised by the Finnish Financial Supervisory Authority. Enable Banking acts as the App's payment-data processor. See their [privacy policy](https://enablebanking.com/privacy-policy/) for details on their own processing.

Beyond Enable Banking and the banks the owner chooses to connect, the App does **not** transmit data to any other party. There are no third-party analytics, error-reporting services, or CDNs that receive any data.

## 6. International transfers

Data flows are confined to the European Economic Area: Enable Banking is established in Finland, and the banks the owner connects must hold a PSD2 licence in an EEA member state.

## 7. Retention

- Bank session metadata is retained until the consent expires (Enable Banking sets this to a maximum of 180 days under PSD2) or until the owner clicks **Disconnect**, whichever happens first.
- Application logs are retained until the owner deletes them. There is no automatic log-rotation policy built into the App.
- Live balance and transaction data is not retained at all between page loads.

To delete all locally-held data, stop the App and remove the `data/` directory.

## 8. The owner's rights

Even where the household exemption applies and the GDPR does not formally engage, the owner retains complete practical control over all data the App holds:

- direct read access to the local H2 database (`SELECT * FROM bank_session;` is the authoritative copy),
- erasure via the **Disconnect** button or by deleting the `data/` directory,
- revocation of bank consent at any time directly with Enable Banking's control panel or with the bank.

No third party other than Enable Banking and the connected banks holds any data on the owner's behalf.

## 9. Security

- API credentials to Enable Banking are authenticated with a JWT signed by an RSA private key that lives only on the owner's machine.
- The local database file is not encrypted by default; rely on full-disk encryption (FileVault, LUKS, BitLocker) for protection at rest.
- The App is intended to be run on `localhost` only by the owner. Exposing it on a public interface, or sharing access with any other person, is outside the App's intended use and is **not** a supported configuration.

## 10. Changes to this policy

Material changes will be reflected in this file in the project repository. The "Last updated" date at the top will be revised accordingly.

## 11. Contact

For questions about this policy, contact asgarov1@gmail.com.
