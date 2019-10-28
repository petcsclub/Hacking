title: SQL Injections

<style>
    .codehilite .s1 {
        background-color: #F0FFF0;
    }
    .codehilite .err {
        color: #FF0000;
        background-color: #FFAAAA;
    }
</style>

# SQLi

## What is SQLi?

Simply put, SQLi enables us to inject custom (malicious) SQL commands. According to [OWASP](https://www.owasp.org/index.php/Main_Page), SQLi was listed as the #1 of its top [10 web vulnerabilities](https://www.owasp.org/images/7/72/OWASP_Top_10-2017_%28en%29.pdf.pdf) list.

## Attack Types/Categories

### String-Based Attacks
!!! In-Band
    In an in-band SQLi attack, the attacker uses the same channel to perform the attack and to receive data about the attack. Here, we have direct, explicit, feedback during the attack.

a

!!! note "Blind/Inferential"
    During a blind SQLi attack, the attacker has no immediate feedback. Instead, we must observe the server responses and behavior in order to learn more about the server's structure.

a

!!! Out-of-Band
    This is an alternative to inferential time-based techniques, especially if the server responses are not very stable (making an inferential time-based attack unreliable). For instance, we can force the victim to send a request to an attacker-controlled server using MS-SQL's `xp_dirtree`.
    

