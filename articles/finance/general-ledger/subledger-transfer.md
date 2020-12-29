---
title: تحويل دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام
description: يصف هذا الموضوع القدرات في Microsoft Dynamics 365 Finance المرتبطة بعمليه التحويل بدفتر الأستاذ الفرعي في دفتر الأستاذ العام.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7addb1f26a33db84d947e6fede876be648d2c654
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645159"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>تحويل دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع القدرات في Microsoft Dynamics 365 Finance المرتبطة بقواعد تحويل مجموعات من إدخالات دفتر يوميه بدفتر الأستاذ الفرعي.

في الإصدار 8.1، تم إجراء تغييرات للسماح بنقل القواعد، التي أهملت الخيار **متزامن**. للحصول على مزيد من المعلومات راجع [الميزات المهلكة أو التي تمت إزالتها لـ Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).

تتوفر الخيارات التالية لنقل مجموعات بدفتر الأستاذ الفرعي. 

 - غير متزامن-سيقوم هذا الخيار علي الفور بجدوله تحويل إدخالات المحاسبة بدفتر الأستاذ الفرعي إلى دفتر الأستاذ العام. سيتم تسجيل إيصال دفتر الأستاذ العام بمجرد ان تكون الموارد حره لمعالجه هذا الطلب علي الخادم. 

- المجموعة المجدولة-سيقوم هذا الخيار باضافه الإدخالات المحاسبية لدفتر الأستاذ الفرعي التي يتم تحويلها إلى قائمه انتظار المعالجة في دفتر الأستاذ العام ، حيث ستتم معالجه الإدخالات بالترتيب الذي تم استلامه. سيتم تسجيل إيصال دفتر الأستاذ العام في الوقت المجدول إذا كانت الموارد حره لمعالجه وظيفة الدفعة هذه علي الخادم. 
 
في إصدار 10.0.8، تم اجراء تحسينات لتحسين أداء الخيار غير المتزامن. يتم تمكين هذه الميزة ضمن اسم الميزة **تحسين أداء تحويل دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام**. 
 
تعمل هذه الوظيفة علي تحسين نقل البيانات من دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام. وهو يسمح بان تكون العملية أكثر فعاليه ، كما انها تقوم بتجميع مجموعات من الحركات الأصغر لنقلها. وهذا يسمح باستخدام خادم المجموعة بكفاءة أكبر. تتطلب هذه الوظيفة اعداد خادم المجموعة والاتصال بالإنترنت لكي يعمل خيار التحويل غير المتزامن. 
