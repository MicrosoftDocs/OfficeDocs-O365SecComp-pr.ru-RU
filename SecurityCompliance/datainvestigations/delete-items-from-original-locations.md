---
title: Удаление элементов из исходного расположения
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: В этой статье описывается, как использовать новое средство расследования данных (Preview) в центре безопасности & соответствия требованиям для удаления элементов из их исходных расположений.
ms.openlocfilehash: 9c8b7c0707183e9bd0f423790b47f9aa60e35912
ms.sourcegitcommit: 3962de88a143f0eb416b5cfdfd777d731f560ec8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2019
ms.locfileid: "36654174"
---
# <a name="delete-items-from-their-original-location-preview"></a>Удаление элементов из исходного расположения (Предварительная версия)

Функция, позволяющая удалять элементы из исходного места, находится в предварительной версии.

С помощью расследования данных можно удалять элементы из их исходных расположений. Это означает, что вы можете удалять элементы из почтовых ящиков Exchange, сайтов SharePoint и учетных записей OneDrive в Организации. Так как вы собрали элементы в качестве свидетельства, у вас есть копии элементов, сохраненных в наборе свидетельств для дальнейшего исследования или сохранения в качестве справочных материалов.

## <a name="before-you-begin"></a>Перед началом работы

- Чтобы удалить элементы, необходимо назначить роль " **Поиск и очистка** " в центре безопасности & соответствия требованиям. Эта роль назначается по умолчанию встроенной группе ролей Data Инвестигатор. 

- В процедуре, описанной в этом разделе, предполагается, что вы выполнили поиск, связанный с исследованием, и добавили результаты поиска в набор свидетельств. После того как результаты поиска будут иметь свидетельство, можно выбрать один или несколько элементов для удаления. Для получения дополнительных сведений обратитесь к разделу [Поиск данных при расследовании](search-for-data.md).

- Важно помнить, что удаляются только элементы из исходных расположений содержимого (например, почтовые ящики Exchange, сайты SharePoint и учетные записи OneDrive). Эти элементы не удаляются из набора свидетельств. Это связано с тем, что элементы в наборе свидетельства являются копиями исходного объекта. Эти элементы копируются при добавлении результатов поиска в набор свидетельств.

## <a name="delete-items"></a>удалять элементы.

Чтобы удалить элементы из исходного расположения, выполните следующие действия:

1. В средстве **расследования данных** откройте исследование данных, содержащее элементы, которые необходимо удалить, а затем перейдите на вкладку **свидетельство** .

2. Выберите элементы, которые требуется удалить. Вы можете выбрать все элементы в наборе свидетельств или выбрать только подмножество элементов. 

   > [!NOTE]
   > Если вы выбираете вложения электронной почты или файла, вложенного в документ, в SharePoint и OneDrive, родительский элемент также будет выбран и удален при удалении элемента из исходного расположения. Аналогично, если выбрать элемент с вложениями, родительский элемент элемента и все вложения удаляются.
 
2. Щелкните **действие** , а затем щелкните **удалить элементы из исходных расположений**.

   ![Щелкните действие, а затем выберите команду Удалить элементы из исходных расположений.](../media/DataInvestigationsDeleteItems1.png)

3. На всплывающей странице проверьте количество элементов и связанных дочерних документов, которые будут удалены, а затем нажмите кнопку **Удалить**.

   ![На всплывающей странице отображается количество элементов и вложенных документов, выбранных для удаления](../media/DataInvestigationsDeleteItems2.png)

   > [!NOTE]
   > В предыдущем снимке экрана количество элементов указывает количество элементов, выбранных для удаления. Число документов указывает на общее количество элементов, включая все файлы, вложенные в родительский элемент. Например, если вы выбрали одно сообщение электронной почты и у него есть вложенный документ Word, то количество элементов и документов, отображаемых в списке **Выбранные документы** , будет равно **1 элементу (2 документа)**.

Вы можете отслеживать ход выполнения задания " **Удаление элементов из исходного расположения** " на вкладке " **задания** ". щелкните задание, чтобы отобразить раскрывающуюся страницу. 

![Всплывающая страница для задания "удаление элементов из исходного расположения"](../media/DataInvestigationsDeleteItems3.png)

При удалении элементов в задании задано состояние " **успешно**". Кроме того, отображается время и Дата выполнения задания. 

![Задание по завершению удаления элементов](../media/DataInvestigationsDeleteItems4.png)

> [!NOTE]
> Вы можете получить состояние " **частично успешно** " для задания " **удалить элементы из исходного расположения** ". Существует несколько ситуаций, которые привели к этому состоянию задания. Для получения дополнительных сведений обратитесь к разделу [частично успешно выполненных удалений](#partially-successful-deletions) этой статьи.

## <a name="what-happens-when-you-delete-items"></a>Что происходит при удалении элементов

В настоящее время при удалении элементов из исходного расположения содержимого элементы будут *обратимо удалены*. Это означает, что элементы перемещаются в специальное расположение и сохраняются до истечения срока хранения удаленных элементов, а элемент помечается для постоянного удаления из Office 365. Обратимое удаление элементов означает, что пользователи все еще могут восстановить эти элементы, пока не истечет срок хранения. Ниже приведены описания того, что происходит при обратимом удалении элементов из почтовых ящиков Exchange и сайтов SharePoint и OneDrive для бизнеса, а также о действиях пользователей после удаления элементов из их исходных расположений.

- **Почтовые ящики:** При обратимом удалении элемента почтового ящика он перемещается в папку "элементы с возможностью восстановления" в почтовом ящике. Это поведение аналогично тому, как пользователь удаляет элемент из папки "Удаленные" или окончательно удаляет элемент, нажимая клавиши Shift + Delete. На этом шаге пользователь может восстановить элемент вплоть до истечения срока хранения удаленных элементов. В Office 365 срок хранения удаленных элементов по умолчанию составляет 14 дней, но администратор может увеличить срок хранения до 30 дней. По истечении срока хранения элемент перемещается в скрытую папку (называемую папкой *очистки* ). Элемент окончательно удаляется из Office 365 при следующем обработке почтового ящика. Почтовые ящики обрабатываются один раз в семь дней).

- **Сайты SharePoint и OneDrive:** Когда файл или документ на сайте является обратимым удалением, он перемещается в корзину сайта (также называется корзиной *первого этапа* ). Элемент остается в корзине в течение 93 дней (срок хранения удаленных элементов для сайтов в Office 365). В течение 93-дневного периода удаленные элементы по-прежнему могут быть восстановлены администратором семейства веб-сайтов в SharePoint или пользователем или администратором в OneDrive. В корзине первого уровня также можно удалять элементы. Когда это происходит, элементы перемещаются в корзину для семейства веб-сайтов, которое называется корзиной *второго уровня* . Срок хранения составляет 93 дней для корзины первого и второго стадий. Это означает, что время хранения корзины второго уровня начинается при первоначальном удалении элемента. Это означает, что общее максимальное время хранения составляет 93 дней для обоих корзин. Если элемент удален из корзины второго уровня (вручную администратором или автоматически по истечении срока хранения), он больше не доступен администратору.

## <a name="what-happens-if-a-content-location-is-on-hold"></a>Что произойдет, если расположение содержимого находится на удержании

В Office 365 почтовые ящики и сайты можно разместить на удержании или назначить политике хранения. Это означает, что ничто не удаляется без возможности восстановления до истечения срока хранения элемента или до удаления удержания. Даже при удалении элемента из исходного расположения его нельзя окончательно удалить из Office 365. Например, если почтовый ящик находится на удержании, обратимо удаленные элементы перемещаются в папку очистки или DiscoveryHold в папке "элементы с возможностью восстановления" и сохраняются до истечения срока хранения или периода хранения. Для сайтов копия элемента, перемещенного в корзину, копируется в библиотеку хранения хранения, которая создается, когда на сайт размещается политика хранения или хранения.

## <a name="partially-successful-deletions"></a>Частично успешное удаление

После завершения выполнения задания " **Удаление элементов из исходного расположения** " вы можете получить состояние " **частично успешно**". Как правило, это состояние указывает на то, что задание выполнено успешно, но не все элементы были удалены с возможностью восстановления. Вот список причин, в результате которых частичное успешное удаление:

- Элемент почтового ящика уже находится в папке "элементы с возможностью восстановления" в исходном почтовом ящике.

- Элемент почтового ящика был удален из папки "элементы с возможностью восстановления" в исходном почтовом ящике.

- Документ уже был размещен в корзине первого уровня на сайте SharePoint или OneDrive.

- После добавления в набор свидетельств документ был перемещен на другой сайт SharePoint. В этом случае документ не перемещается в корзину на сайте, на который он был перемещен.

- Документ был окончательно удален в SharePoint или OneDrive (перемещен в корзину второго уровня) после добавления в набор свидетельств.