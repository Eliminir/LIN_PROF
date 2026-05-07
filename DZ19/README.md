
# 1. Проброс порта работает
curl http://192.168.100.2:8080

# 2. Без knock порт 22 закрыт
sudo ip netns exec centralRouter nc -zv 192.168.255.1 22

# 3. Выполняем knock (стучим в порты)
sudo ip netns exec centralRouter bash -c "nc -w 1 -z 192.168.255.1 1234 && nc -w 1 -z 192.168.255.1 5678 && nc -w 1 -z 192.168.255.1 9012"

# 4. После knock IP появляется в AUTH списке
sudo ip netns exec inetRouter cat /proc/net/xt_recent/AUTH

# 5. HTTP сервер на centralServer работает
sudo ip netns exec centralServer curl localhost:80
