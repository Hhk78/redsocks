```
base {
    log_debug = on;
    log_info = on;
    log = "file:./redsocks.log";

    daemon = on;

    redirector = iptables;
}

redsocks {
    local_ip = 0.0.0.0;
    local_port = 12345;

    ip = $proxy_ip;
    port = $proxy_port;

    type = $proxy_type;

    login = "$proxy_user";
    password = "$proxy_passwd";
}
```
