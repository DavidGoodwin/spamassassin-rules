# spamassassin-rules

Random spamassassin rules. They're a subset of those I use for work. They may not work for you or do anything useful.

They (should) all have a PP\_ prefix ...

# installation

Copy rules/* to /etc/spamassassin ... there are probably better ways but this works for me.

Restart SpamAssassin if necessary.

# testing

```
cd rules ; spamassassin --lint -L -t -C . 
cp rules/* /etc/spamassassin/
cat /path/to/some/email.txt | spamassassin -tL ```
```
or

``` spamassassin -tLD < /path/to/some/email.txt 2>&1 | grep PP_```
