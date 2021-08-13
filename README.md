# mailserver-arm
Container base ARM mail server from https://docker-mailserver.github.io

1. Update the enviornment mailserver.env file with your own values

2. If running this behind NAT port forward:
      - "25:25"    # SMTP  (explicit TLS => STARTTLS)
      - "143:143"  # IMAP4 (explicit TLS => STARTTLS)
      - "465:465"  # ESMTP (implicit TLS)
      - "587:587"  # ESMTP (explicit TLS => STARTTLS)
      - "993:993"  # IMAP4 (implicit TLS)

3. usage:
docker-compose -f /opt/mailserver-arm/mailserver-arm-compose.yml -d

4. Use setup.sh to create accounts, aliases and other administration tasks