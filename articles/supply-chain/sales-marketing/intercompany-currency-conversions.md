---
title: تحويلات العملات بين الشركات الشقيقة
description: يشرح هذا الموضوع تحويلات العملات للحركات بين الشركات الشقيقة
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548088"
---
# <a name="intercompany-currency-conversions"></a>تحويلات العملات بين الشركات الشقيقة

[!include [banner](../../includes/banner.md)]

عندما اختلاف كود العملة على أمر المبيعات الأصلي وأمر الشراء بين الشركات الشقيقة، يتم تحويل العملة في الحقول التالية إذا تم تمكين التزامن:

- **سعر الوحدة**
- **مصاريف المبيعات‬** أو **تكاليف المشتريات‬**
- **الخصم**
- **خصم متعدد الأسطر**

بعد ذلك، تتم مزامنة هذه الحقول مع بند أمر المبيعات الأصلي.

ومع ذلك، وبسبب مزامنة العمل على أمر الشراء بين الشركات الشقيقة وأمر المبيعات بين الشركات الشقيقة دائمًا، تتم مزامنة الحقول التالية من دون تحويل العملة:

- **سعر الوحدة**
- **مصاريف المبيعات‬** أو **تكاليف المشتريات‬**
- **الخصم**
- **نسبة الخصم**
- **خصم متعدد الأسطر**
- **نسبة خصم متعددة الأسطر**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
