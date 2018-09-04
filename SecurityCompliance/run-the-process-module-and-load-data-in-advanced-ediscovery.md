---
title: Запуск модуля обработки и загрузка данных в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Сведения об использовании безопасности Office 365 &amp; центре соответствия требованиям для доступа к Office 365 расширенного обнаружения электронных данных и запуска модуля процесса для обращения.  '
ms.openlocfilehash: 32052bccc37d20c8707a1efb0592f7c93daf3590
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534858"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a>Запуск модуля обработки и загрузка данных в Office 365 Advanced eDiscovery

> [!NOTE]
> Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
В этом разделе описываются функциональные возможности модуля процесса расширенной обнаружения электронных данных. 
  
В дополнение к данным файл метаданных, такие как тип файлов, расширение, расположение или путь, Дата создания и время, автора, custodian и темы, могут быть загружены в расширенного обнаружения электронных данных и сохранения для каждого случая. Некоторые метаданные рассчитывается по расширенной eDiscovery, например при загрузке собственный файлов. 
  
Расширенные eDiscovery предоставляет системы значения метаданных, например группирование почти повторяющиеся или показателям релевантности. Можно добавить других метаданных, например файл аннотации администратором. 
  
## <a name="running-process"></a>Запуск процесса

> [!NOTE]
> Чтобы разрешить отслеживание файлы назначаются номера пакета в файл во время процесса. Номер пакета также позволяет Идентификация обработка пакетов для повторной обработки параметров. Для фильтрации, номер партии и сеансы доступны дополнительные фильтры. 
  
Выполните следующие действия, чтобы запустить процесс.
  
1. [Откройте безопасности Office 365 &amp; центре соответствия требованиям](go-to-the-securitycompliance-center.md) . 
    
2. Последовательно выберите пункты **поиска &amp; расследования** \> **обнаружения электронных данных** и нажмите кнопку **Перейти к расширенной обнаружения электронных данных**.
    
3. В расширенной eDiscovery выберите соответствующий регистр в отображаемой страницы **случаев** и нажмите кнопку **Перейти на случай**.
    
4. В статье **Prepare** \> **процесс** \> **программы установки**, выберите контейнер из списка доступных контейнеров.
    
    ![Щелкните процесс, чтобы добавить результаты поиска в рамках данного экземпляра](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. Нажмите кнопку **Дополнительные параметры...** , если вы хотите добавить в контейнер как файлы начального значения или как предварительно с тегами файлы. 
    
    Использовать файлы начального значения для ускорения обучающие курсы по проблемы с низкой расширение (обычно % 2, или меньше). Для файлов, начального значения, рекомендуется выбрать различные явно соответствующие файлы и обработки о исходные значения 20-50 на проблему (слишком много файлов начального значения можно изменяют релевантности результатов). Начальное значение файлы следует изучить с одного человека, который будет обучение пользователей проблему.
    
    Используйте предварительно с тегами файлы для автоматизации учебный курс по релевантности. Следует отметить по крайней мере 1 500 файлы и сохранить пропорции относится к не соответствующие файлы такой же, как увеличить значимость коллекции. Эти файлы должны быть вручную с тегами и должны быть уверенным в качестве тегов.
    
    ![Снимок экрана Дополнительные параметры страницы для обработки файлов пакета](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - В разделе **начального значения** : 
    
    Выберите **Пометить как файлы начальное значение** для контейнера отметить как файлы начального значения. Вы также должны выбрать назначать их на проблему с **проблемы** раскрывающемся списке. Выберите из раскрывающегося списка **тег** **Relevant** или **не соответствующие** . 
    
    > [!NOTE]
    > После установки файлов в качестве **начального значения**их нельзя пометить как **предварительно с меткой**. 
  
  - В разделе **предварительно с тегами файлы** : 
    
    Выберите **Пометить как предварительно с тегами файлы** пометку контейнер, предварительно с тегами файлы. Также необходимо назначить их на проблемы **по вопросам** раскрывающемся списке. Выберите из раскрывающегося списка **тег** **Relevant** или **не соответствующие** . 
    
    > [!NOTE]
    > После установки файлов как **предварительно с меткой**, их нельзя пометить как **начального значения**. 
  
  - В разделе **тегов электронной почты** . набор, какую часть обработанные электронной почты, которую надо отметить как инициирующий или предварительно с тегами. 
    
6. Чтобы приступить к работе, щелкните **процесс**. После завершения процесса результаты отображаются.
    
7. (Необязательно) Если им необходимо назначить источников данных для конкретных custodian, можно добавлять и редактировать имена custodian в **Custodians** \> **Управление** и назначить custodians в **Custodians** \> **назначения**. 
    
Если вы добавили в случае, затем можно обрабатывать еще раз.
  
## <a name="see-also"></a>См. также

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Просмотр результатов процесса модуля](view-process-module-results-in-advanced-ediscovery.md)
