# Bad email domains & addresses list

This repository contains a manually curated list of **bad email domains** and **email addresses** that have been identified in association with **spam**, **phishing**, **fraud**, and other malicious activities. These entries have been gathered from various sources, including abuse reports, spam traps, and other cybersecurity resources.

## Purpose

The purpose of this repository is to provide a list of suspicious or malicious email domains and addresses to help:
- Block or filter out known bad actors from email systems.
- Prevent phishing attempts, email scams, and other forms of email-based abuse.
- Enhance email security by integrating the list into email filtering systems, firewalls, and security tools.

## Usage

There are several ways you can use the list to protect your email infrastructure:

1. **Email Filtering**: Integrate the list into your email server's filtering system (e.g., **Postfix**, **Exim**, **SpamAssassin**) to automatically reject or flag incoming messages from bad email domains or addresses.

    Example with Postfix:
    ```bash
    smtpd_sender_restrictions = check_sender_access hash:/etc/postfix/bad_senders
    ```

    Example entry in `/etc/postfix/bad_senders`:
    ```
    bademail@example.com  REJECT
    bad-domain.com        REJECT
    ```

2. **Spam Filter Enhancement**: Use the email addresses and domains to train spam filters and improve detection of phishing or malicious messages.

3. **Monitoring**: Use the list to monitor email traffic for any attempts to interact with these known bad addresses or domains, allowing for proactive action.

## Format

The repository contains two text files:
1. **bad_email_addresses.txt**: Contains email addresses, with one address per line.
2. **bad_email_domains.txt**: Contains email domains, with one domain per line.

This format allows for easy integration into scripts or security tools.

## Contribution

We welcome contributions from the community! If you encounter email addresses or domains involved in spam, phishing, or malicious activities, feel free to submit them. Please ensure that any submission is verified and include any relevant details on how the address or domain was identified as bad.

## Disclaimer

This list is provided **as is** and may not be comprehensive or up to date. While the entries are known to be involved in malicious activities at some point, the behavior of these domains and email addresses may change over time. It's recommended to review and validate the entries before taking action based solely on this list.
