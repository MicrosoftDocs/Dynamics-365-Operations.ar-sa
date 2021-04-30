---
title: تحويل دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام
description: يصف هذا الموضوع القدرات في Microsoft Dynamics 365 Finance المرتبطة بعمليه التحويل بدفتر الأستاذ الفرعي في دفتر الأستاذ العام.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897494"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>تحويل دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع القدرات في Microsoft Dynamics 365 Finance المرتبطة بقواعد تحويل مجموعات من إدخالات دفتر يوميه بدفتر الأستاذ الفرعي.

في الإصدار 8.1، تم إجراء تغييرات للسماح بنقل القواعد، التي أهملت الخيار **متزامن**. للحصول على مزيد من المعلومات راجع [الميزات المهلكة أو التي تمت إزالتها لـ Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

تتوفر الخيارات التالية لنقل مجموعات بدفتر الأستاذ الفرعي. 

 - غير متزامن-سيقوم هذا الخيار علي الفور بجدوله تحويل إدخالات المحاسبة بدفتر الأستاذ الفرعي إلى دفتر الأستاذ العام. سيتم تسجيل إيصال دفتر الأستاذ العام بمجرد ان تكون الموارد حره لمعالجه هذا الطلب علي الخادم. 

- المجموعة المجدولة-سيقوم هذا الخيار باضافه الإدخالات المحاسبية لدفتر الأستاذ الفرعي التي يتم تحويلها إلى قائمه انتظار المعالجة في دفتر الأستاذ العام ، حيث ستتم معالجه الإدخالات بالترتيب الذي تم استلامه. سيتم تسجيل إيصال دفتر الأستاذ العام في الوقت المجدول إذا كانت الموارد حره لمعالجه وظيفة الدفعة هذه علي الخادم. 
 
في إصدار 10.0.8، تم اجراء تحسينات لتحسين أداء الخيار غير المتزامن. يتم تمكين هذه الميزة ضمن اسم الميزة **تحسين أداء تحويل دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام**. 
 
تعمل هذه الوظيفة علي تحسين نقل البيانات من دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام. وهو يسمح بان تكون العملية أكثر فعاليه ، كما انها تقوم بتجميع مجموعات من الحركات الأصغر لنقلها. وهذا يسمح باستخدام خادم المجموعة بكفاءة أكبر. تتطلب هذه الوظيفة إعداد خادم المجموعة والاتصال بالإنترنت لكي يعمل خيار التحويل غير المتزامن. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]