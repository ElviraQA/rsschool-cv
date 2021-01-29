# Elvira Semenova

Located in **Moscow, Russia**  
**+7 995 502–33–79  
[semenovaelviraa@gmail.com](mailto:semenovaelviraa@gmail.com)**

Portfolio at **[portfolio site](https://github.com/ShalopaykaQA)**

## Summary

I’m going to start working as a Junior QA in IT company this year. This is my first step in the area, where people 
create big useful things and make high demands on quality their products. In spite of my work experience and education, 
I have always been attracted to the IT, and now, finally, it's time when I can afford to do what I really like. 
I always learn for being more productive, because with more experience and the necessary skills, I hope to move to developers.

I'm well-organized, responsible person with good communication skills and positive wives on life. I always try to 
figure out the better way to do anything, constantly increasing quality of my work.

## Experience and education

**Graduated** 
 
*2000 - 2006* BA in Law, Humanitarian University, Yekaterinburg.

*2015 - 2016* Certificate in Project Management, Moscow International Higher School of Business MIRBIS          

**Self-education:**
* Completed [www.w3schools.com (HTML and CSS)](https://www.w3schools.com/default.asp) (and marksheet.io, www.htmldog.com)
* Completed [Netology:Introduction to testing](https://u.netology.ngcdn.ru/backend/uploads/legacy/shared_diplomas/pdf_certificate/46073/certificate.pdf)
* Completed [Netology:Git-version control system](https://u.netology.ngcdn.ru/backend/uploads/legacy/shared_diplomas/pdf_certificate/46993/certificate.pdf)
* Completed [Netology:Java for Testers](https://u.netology.ngcdn.ru/backend/uploads/legacy/shared_diplomas/pdf_certificate/53152/certificate.pdf)
* Studying  [job4j:Java](https://job4j.ru/edu/) (now on collections)
* Studying  [learn.epam.com:Software Testing Introduction](https://learn.epam.com/detailsPage?id=a4a1b6e2-4e51-455d-ac5b-e60f23d4ed69)

**Working on [portfolio site](https://github.com/ShalopaykaQA)**  
*since 2020, nowdays*

## Code examples

**[portfolio site](https://github.com/ShalopaykaQA)**

```
package ru.job4j.bank;

import java.util.ArrayList;
import java.util.HashMap;
import java.util.List;
import java.util.Map;

/**
 * Класс хранит всех пользователей и их счета.
 * Реализует функционал перевода денег.
 *
 * @author Эльвира (mailto:shalopayka@gmail.com).
 * @version 1.
 * @since 29.12.2020.
 */
public class BankService {
    private Map<User, List<Account>> users = new HashMap<>();

    /**
     * Метод реализует добавление нового клиента.
     *
     * @param user Новый пользователь, которого нужно добавить.
     */
    public void addUser(User user) {
        users.putIfAbsent(user, new ArrayList<Account>());
    }

    /**
     * Метод реализует добавление нового счета клиенту.
     *
     * @param passport Паспортные данные клиента, которому нужно добавить счет.
     * @param account  Новый счет, который нужно добавить.
     */
    public void addAccount(String passport, Account account) {
        User user = findByPassport(passport);
        if (user != null) {
            if (!users.get(user).contains(account)) {
                users.get(user).add(account);
            }
        }
    }

    /**
     * Метод реализует получение счета клиента по паспорту клиента и реквизитам.
     *
     * @param passport Паспортные данные клиента, счет которого нужно получить.
     * @return Возвращает клента. Если клиента нет, возвращает пустой объект.
     */
    public User findByPassport(String passport) {
        User rsl = null;
        for (User user : users.keySet()) {
            if (user.getPassport().equals(passport)) {
                rsl = user;
                break;
            }
        }
        return rsl;
    }

    /**
     * Метод реализует получение счета клиента по паспорту клиента и реквизитам.
     *
     * @param passport  Паспортные данные клиента, счет которого нужно получить.
     * @param requisite Реквизиты счета, который нужно получить.
     * @return Возвращает счет. Если счета нет, возвращает пустой объект.
     */
    public Account findByRequisite(String passport, String requisite) {
        Account rsl = null;
        User user = findByPassport(passport);
        if (user != null) {
            List<Account> accounts = users.get(user);
            for (Account account : accounts) {
                if (account.getRequisite().equals(requisite)) {
                    rsl = account;
                    break;
                }
            }
        }
        return rsl;
    }

    /**
     * Метод реализует перевод денег между счетами.
     *
     * @param srcPassport   Паспортные данные клиента, со счета которого нужно перевести деньги.
     * @param srcRequisite  Реквизиты счета, с которого нужно перевести деньги.
     * @param destPassport  Паспортные данные клиента, на счет которого нужно перевести деньги.
     * @param destRequisite Реквизиты счета, на который нужно перевести деньги.
     * @param amount        Сумма денег, которую нужно перевести.
     * @return true, если перевод успешен, в противном случае вренет false.
     */
    public boolean transferMoney(String srcPassport, String srcRequisite,
                                 String destPassport, String destRequisite, double amount) {
        boolean rsl = false;
        Account srcAccount = findByRequisite(srcPassport, srcRequisite);
        Account destAccount = findByRequisite(destPassport, destRequisite);
        if (srcAccount != null && destAccount != null && srcAccount.getBalance() >= amount) {
            destAccount.setBalance(destAccount.getBalance() + amount);
            srcAccount.setBalance(srcAccount.getBalance() - amount);
            rsl = true;
        }
        return rsl;
    }
}
```

## Skills

◾◾◾◾◽ HTML    
◾◾◾◽◽ CSS   
◾◾◾◾◾ The theory of software testing    
◾◾◾◾◽ GIT   
◾◾◾◽◽ MySQL  
◾◾◾◽◽ Postman   
◾◾◾◽◽ JMeter  
◾◾◽◽◽ Java    

## English level is B2

**Or Upper-Intermediate** in accordance [Training test results](https://)

## Contact me

E-mail: [semenovaelviraa@gmail.com](mailto:semenovaelviraa@gmail.com)

Phone: +7 995 502–33–79