# Secrets

This section contains stuff on secret management/gpg/ssh/yubikey/etc

## Links

* [Yubikey Guide](https://github.com/drduh/YubiKey-Guide)
* [Yubikey Agent](https://github.com/FiloSottile/yubikey-agent)


## How To

### Open a connection to auth agent and add resident ssh identity

1. Start the ssh agent

```
eval ssh-agent $SHELL
```

2. Add the resident identity from yubikey

```
ssh-add -K
```

Enter your pin and you are done. Output will be like

```
❯ ssh-add -K
Enter PIN for authenticator: 
Resident identity added: ECDSA-SK SHA256:6451MOXmAplsLFnosKOozJ/R0TkpsaxDUT1HddSwfYg
```

