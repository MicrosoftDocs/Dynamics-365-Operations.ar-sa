---
title: تحويلات العملات بين الشركات الشقيقة
description: يشرح هذا المقال تحويلات العملات للحركات بين الشركات الشقيقة
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851467"
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
