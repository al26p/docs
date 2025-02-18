---
title: 'Aktywacja weryfikacji dwuetapowej za pomocą klucza sprzętowego'
excerpt: 'Dowiedz się, jak zabezpieczyć swój panel klienta OVHcloud, aktywując weryfikację dwuetapową za pomocą klucza sprzętowego U2F'
updated: 2024-02-02
---

> [!primary]
> Tłumaczenie zostało wygenerowane automatycznie przez system naszego partnera SYSTRAN. W niektórych przypadkach mogą wystąpić nieprecyzyjne sformułowania, na przykład w tłumaczeniu nazw przycisków lub szczegółów technicznych. W przypadku jakichkolwiek wątpliwości zalecamy zapoznanie się z angielską/francuską wersją przewodnika. Jeśli chcesz przyczynić się do ulepszenia tłumaczenia, kliknij przycisk "Zgłóś propozycję modyfikacji" na tej stronie.
>

## Wprowadzenie

Weryfikacja dwuetapowa za pomocą klucza sprzętowego Universal Second Factor (U2F) to jedna z oferowanych przez OVHcloud metod zabezpieczenia dostępu do konta. Ta technika zabezpieczeń z użyciem klucza USB, coraz częściej stosowana do weryfikacji dwuetapowej w różnych zastosowaniach, należy do FIDO Alliance.

**Niniejszy przewodnik pozwoli Ci aktywować weryfikację dwuetapową za pomocą klucza U2F i zrozumieć, jak z niej korzystać podczas następnych logowań do panelu klienta.**

## Wymagania początkowe

- Zapoznanie się z [różnymi metodami weryfikacji dwuetapowej w OVHcloud](/pages/account_and_service_management/account_information/secure-ovhcloud-account-with-2fa).
- Dostęp do [panelu klienta OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pl/&ovhSubsidiary=pl){.external}.
- Posiadanie klucza sprzętowego U2F.
- Dostępność wolnego portu USB w Twoim komputerze.

## W praktyce

### Etap 1: włączenie weryfikacji dwuetapowej

Zaloguj się do [panelu klienta OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pl/&ovhSubsidiary=pl){.external}, kliknij Twoją nazwę użytkownika w prawym górnym rogu (1) i wybierz `Moje konto`{.action} (2). Następnie kliknij `Bezpieczeństwo`{.action} (3), a na koniec `Aktywuj weryfikację dwuetapową`{.action} (4).

![2FA securitykey](images/hub2FA.png){.thumbnail}

### Etap 2: Wybór metody z wykorzystaniem klucza sprzętowego

Wybierz metodę z wykorzystaniem klucza sprzętowego i zatwierdź.

![2FA securitykey](images/2fakey1edit.png){.thumbnail}

### Etap 3: zatwierdzenie weryfikacji dwuetapowej

Podłącz klucz sprzętowego, gdy otrzymasz taki monit. Jeśli jest on wyposażony w przycisk, naciśnij go. 

![2FA securitykey](images/2fakey2.png){.thumbnail}

> [!warning]
>
> Otworzy się okno pop-up z prośbą o zatwierdzenie klucza. Jeśli to okno nie jest widoczne, sprawdź, czy przeglądarka ich nie blokuje.

Po rozpoznaniu klucza możesz także dodać opis. Pomoże on w razie potrzeby zidentyfikować osoby mogące korzystać z tej metody uwierzytelniania na Twoim koncie.

![2FA securitykey](images/2fakey3.png){.thumbnail}

### Etap 4: zachowanie kodów bezpieczeństwa

Przy pierwszym dodaniu metody zabezpieczeń w postaci weryfikacji dwuetapowej otrzymasz kody zapasowe. Należy je zachować w bezpiecznym miejscu. Zalecamy, by przechowywać je w menedżerze haseł.

![2FA securitykey](images/2facodes.png){.thumbnail}

Możesz je usunąć lub wygenerować ponownie w panelu klienta:

![2FA securitykey](images/2facodesaction.png){.thumbnail}

> [!warning]
>
> Przypominamy o konieczności zachowania tych kodów bezpieczeństwa i upewnienia się, że są one prawidłowe. W razie niedostępności wybranej przez Ciebie metody/ metod zabezpieczeń (kradzież bądź utrata telefonu lub klucza bezpieczeństwa), dostęp do Twojego panelu klienta może zostać uniemożliwiony.
> 
> 

### Etap 5: zalogowanie się do panelu klienta z wykorzystaniem weryfikacji dwuetapowej

Po aktywacji uwierzytelniania z wykorzystaniem weryfikacji dwuetapowej na ekranie logowania pojawi się jedna z wybranych przez Ciebie metod zabezpieczeń. Jeśli chcesz skorzystać z innej metody, kliknij przycisk `Wypróbuj inną metodę`{.action}.

![2FA securitykey](images/2fakeylogin.png){.thumbnail}

Pojawią się wówczas wszystkie aktywowane metody.

![2FA securitykey](images/2faloginchoice.png){.thumbnail}

## Sprawdź również

Oficjalna witryna [FIDO Alliance](https://fidoalliance.org/){.external}.

Dołącz do społeczności naszych użytkowników na stronie<https://community.ovh.com/en/>.
