---
title: Быстрая настройка для Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: d7ccd944-9698-41c7-a21b-677dc62973c4
description: 'Сведения о том, как получать доступ к Office 365 Advanced eDiscovery из Центра безопасности и соответствия требованиям Office 365 и просматривать типичный рабочий процесс для использования Advanced eDiscovery.  '
ms.openlocfilehash: 18ba3de9bd8b314eddef90252be532256f0b85a5
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999772"
---
# <a name="quick-setup-for-office-365-advanced-ediscovery"></a>Быстрая настройка для Office 365 Advanced eDiscovery

Этот раздел о настройках содержит сведения для менеджера обнаружения электронных данных в Центре безопасности и соответствия требованиям Microsoft 365 о том, как начать работу с Advanced eDiscovery. Предполагается, что есть общее представление об обеих службах.
  
> [!NOTE]
> Advanced eDiscovery требует наличия Office 365 E3 с надстройкой Advanced Compliance или подписки на E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете [зарегистрироваться для получения пробной версии Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="accessing-a-case-in-advanced-ediscovery"></a>Получение доступа к делу в Advanced eDiscovery

Доступ к Advanced eDiscovery можно получить в Центре безопасности и соответствия требованиям Office 365. Но нужно быть участником дела обнаружения электронных данных в Центре безопасности и соответствия требованиям, чтобы получить доступ к этому делу в Advanced eDiscovery. Сведения о предоставлении разрешений в отношении дела обнаружения электронных данных и добавлении пользователей для такого дела см. в статье [Управление делами обнаружения электронных данных в Office 365](manage-ediscovery-cases.md). 
  
Чтобы перейти к делу в Advanced eDiscovery: 
  
1. [Откройте Центр безопасности и соответствия требованиям Office 365](go-to-the-securitycompliance-center.md). 
    
2. Чтобы отобразился список дел в организации, в Центре безопасности и соответствия требованиям выберите **Поиск и исследование** \> **Обнаружение электронных данных**. 
    
3. На странице **Обнаружение электронных данных** нажмите кнопку **Открыть** рядом с названием дела, к которому хотите перейти в Advanced eDiscovery. 
    
4. На странице **Главная** для этого дела выберите **Advanced eDiscovery**.
    
    Отобразится индикатор выполнения **Подключение к Advanced eDiscovery**. После подключения дело откроется в Advanced eDiscovery. 
    
## <a name="workflow"></a>Рабочий процесс

На приведенной ниже схеме показан типичный рабочий процесс для использования дел обнаружения электронных данных и управления ими в Центре безопасности и соответствия требованиям и Advanced eDiscovery. 
  
![На схеме показан рабочий процесс Office 365 Advanced eDiscovery, состоящий из четырех этапов настройки (настройки пользователей и дел, определения данных дела, экспорта и обработки), а также этапов анализа и экспорта на локальный компьютер.](media/76589ccc-789d-4581-b3a8-98d339b05979.png)
  
Этот раздел о настройках содержит сведения о первых четырех этапах рабочего процесса. Описание других этапов см. далее.
  
## <a name="analyze"></a>Анализ

[Анализ данных дела](analyze-case-data-with-advanced-ediscovery.md) идентифицирует и упорядочивает файлы по различным параметрам, обеспечивает использование категории "Темы", отображает результаты. Для получения улучшенных результатов можно настроить функциональность анализа с учетом пользователя. 
  
## <a name="relevance-setup-and-relevance"></a>Настройка релевантности и модуль релевантности

[Настройка релевантности](manage-relevance-setup-in-advanced-ediscovery.md) и [Использование модуля релевантности](use-relevance-in-advanced-ediscovery.md) обеспечивают оценку и обучение релевантности на основе случайной выборки файлов и используют их для реализации решений в процессе прогнозирующего кодирования. Вычисляют и отображают промежуточные результаты, отслеживая статистическую достоверность процесса. Отображают результаты для помощи в принятии решений при просмотре. 
  
## <a name="export"></a>Экспорт

[Экспорт данных дела](export-case-data-in-advanced-ediscovery.md) обеспечивает экспорт результатов и содержимого Advanced eDiscovery для внешней проверки. 
  
## <a name="report"></a>Отчет

[Создание отчетов](run-reports-in-advanced-ediscovery.md) обеспечивает создание выбранных отчетов, связанных с обработкой Advanced eDiscovery. 
  
## <a name="see-also"></a>См. также

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Настройка пользователей и дел](set-up-users-and-cases-in-advanced-ediscovery.md)
  
[Подготовка данных](prepare-data-for-advanced-ediscovery.md)

