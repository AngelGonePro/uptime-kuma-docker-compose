```
cd ~ && \
curl -fsSL -o /tmp/kuma.zip https://github.com/AngelGonePro/uptime-kuma-docker-compose/raw/refs/heads/main/uptime-kuma.zip && \
python3 -c "import zipfile; open('/tmp/deploy-update.sh','wb').write(zipfile.ZipFile('/tmp/kuma.zip').read('uptime-kuma/deploy-update.sh'))" && \
sh /tmp/deploy-update.sh https://github.com/AngelGonePro/uptime-kuma-docker-compose/raw/refs/heads/main/uptime-kuma.zip status-uptimekuma && \
cp /tmp/deploy-update.sh status-uptimekuma/ && chmod +x status-uptimekuma/*.sh && rm -f /tmp/kuma.zip /tmp/deploy-update.sh
```
