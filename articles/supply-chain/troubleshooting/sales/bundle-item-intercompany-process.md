---
title: صنف المجموعة غير مدعوم في عملية بين الشركات الشقيقة
description: صنف المجموعة غير متوفر للشراء. يقوم أمر المبيعات فقط بشراء مكونات صنف المجموعة، وليس صنف المجموعة نفسه.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475474"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>صنف المجموعة غير مدعوم في عملية بين الشركات الشقيقة

## <a name="symptoms"></a>العلامات

لا يتوفر صنف المجموعة لأمر الشراء لأنك، إذا قمت بفحص بنود أمر المبيعات لصنف المجموعة، ستلاحظ أن الكمية هي *0* (صفر) والحالة هي *ملغى*.

## <a name="resolution"></a>الحل

يتم هذا السلوك بسبب التصميم. يشتري أمر المبيعات مكونات صنف المجموعة فقط. ولا يشتري صنف المجموعة بحد ذاته. إذا كان من الضروري شراء مجموعة، فعليك أن تأخذ في الاعتبار ما إذا كان يجب وضع علامة عليه كصنف مجموعة، لأن هذه الوظيفة مصممة بالفعل لسيناريوهات التعرف على الإيرادات. لمزيد من المعلومات حول أصناف المجموعة، راجع [المجموعات](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
