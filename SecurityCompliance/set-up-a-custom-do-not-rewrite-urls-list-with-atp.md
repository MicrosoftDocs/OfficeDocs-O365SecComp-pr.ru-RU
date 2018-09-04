---
title: Настроить пользовательский список not переопределения URL-адресов с помощью Office 365 ATP безопасных ссылки
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
description: При настройке политик безопасных ссылок анализа может включать действие переопределения не "список URL-адресов, чтобы включить некоторые пользователи в вашей организации на сайтах, которые включены в список.
ms.openlocfilehash: 0ee9c87c90e6e30d6c43fb0de5291dd85b03be07
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782166"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a>Настроить пользовательский список not переопределения URL-адресов с помощью Office 365 ATP безопасных ссылки

[Защиту от угроз для Office 365 Advanced](office-365-atp.md) (ATP) ваша организация может иметь [настраиваемые заблокированных URL-адреса](set-up-a-custom-blocked-urls-list-wtih-atp.md), таким образом, когда люди нажмите кнопку на веб-адреса (URL-адреса) в сообщения электронной почты или в некоторых документах Office, они не смогут переход на этих URL-адресов. Организации могут также иметь настраиваемые списки «не rewrite» для определенных групп в организации. Список «не rewrite» позволяет кому посетите URL-адресов, в противном случае — блокирует [ATP безопасных ссылок в Office 365](atp-safe-links.md). 
  
В этой статье описывается, как для указания списка URL-адресов, исключенных из безопасных ссылок анализа сканирования и некоторые важные моменты, которые следует помнить.

## <a name="set-up-a-do-not-rewrite-list"></a>Настройка списка «не rewrite»

Защита от безопасных ссылок анализа использует несколько списков, включая черный список URL-адресов вашей организации и списки «не rewrite» для исключения. При наличии необходимых разрешений можно настроить настраиваемых списков «не rewrite». Для этого после добавления или изменения политики безопасных ссылок, которые применяются к определенным получателям в организации. 
  
1. Последовательно выберите пункты [https://protection.office.com](https://protection.office.com) и войдите с учетной записи рабочего или школы. 
    
2. В левой панели навигации в разделе **Управление угроз** \> **политики** \> **Безопасных ссылки**.
    
3. В разделе **политики, которые применяются к определенным получателям** , нажмите кнопку **Создать** (новой кнопки имеет следующий вид: знак плюс ( **+**)) для создания новой политики. (Кроме того, можно изменить существующую политику.)
    
    ![Нажмите кнопку Создать, чтобы добавить политику безопасных ссылки для конкретных электронной почты получателей](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
4. Укажите имя и описание политики.
    
5. В разделе **не переопределить следующие URL-адреса** выберите поле **Введите допустимый URL-адрес** и введите URL-адрес и затем нажмите знак плюс (+). 
    
6. В разделе **Применить к** выберите **получатель входит в состав**и выберите группы, которые необходимо включить в политике. Последовательно выберите пункты **Добавить**и затем нажмите **кнопку ОК**.
    
7. Завершив добавление URL-адресов, в правом нижнем углу экрана, выберите команду **Сохранить**.
    
> [!NOTE]
> Убедитесь, что для просмотра вашей организации настраиваемый список заблокированных URL-адресов. В разделе [Настройка настраиваемого заблокированных список URL-адресов с помощью безопасных ссылок анализа](set-up-a-custom-blocked-urls-list-wtih-atp.md). 
  
## <a name="important-points-to-keep-in-mind"></a>Важные вопросы, на которые следует помнить

- Любые URL-адресов, указанных в список «не rewrite», исключаются из анализа безопасных ссылки сканирования для получателей можно указать.
 
- При указании список «не rewrite» для политики ATP безопасных ссылок, может включать до трех подстановочные знаки звездочки (\*). Подстановочные знаки (\*) предполагается, что для операций, таких как `contoso.com`, которого не включить явным образом префиксами или дочерние домены, как `http://` или `https://`. Это означает, что записи, такие как `contoso.com` аналогичен `\*contoso.com\*` для списка «не rewrite».

- Если уже имеется список URL-адресов в списке «не rewrite», обязательно просмотрите этот список и добавьте подстановочные знаки соответствующим образом. Например, если имеется существующий список запись, например `http://contoso.com/a` и вы хотите включить субконтуров как `http://contoso.com/a/b` в политике, добавьте подстановочный знак в запись, чтобы он выглядел, как `http://contoso.com/a\*`.
    
- Не включайте в URL-адресов, указанных в списке «не rewrite» косую черту (/). Например вместо ввода `contoso.com/` в список «не rewrite» введите `contoso.com`.
    
В следующих примерах списков в таблице можно ввести и что в силу эти записи имеют.
    
|**Пример записи**|**Описание**|
|:-----|:-----|
|`\*contoso.com\*`  <br/> |Позволяет определенным получателям посетите домена, поддомены и пути, такие как `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, или`http://www.contoso.com/a`  <br/> |
|`http://contoso.com/a`  <br/> |Позволяет определенным получателям, посетите веб-сайт как `http://contoso.com/a`, но не субконтуров`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a\*`  <br/> |Позволяет определенным получателям, посетите веб-сайт как `http://contoso.com/a` и субконтуров, например`http://contoso.com/a/b`  <br/> |
   
  

## <a name="related-topics"></a>Смежные темы

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Безопасно ATP ссылок в Office 365](atp-safe-links.md)
  
[Настройка политик ATP безопасных ссылок в Office 365](set-up-atp-safe-links-policies.md)
  
[Настройка пользовательских заблокированных список URL-адресов с помощью безопасных ссылок анализа](set-up-a-custom-blocked-urls-list-wtih-atp.md)

[Просмотр отчетов для защиты расширенного Threat Office 365](view-reports-for-atp.md)

[Разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md)
  
