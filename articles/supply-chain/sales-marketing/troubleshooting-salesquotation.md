---
title: استكشاف أخطاء عروض أسعار المبيعات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع عروض أسعار المبيعات.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9a9cc821d2fe9accad1dae210271682cdd2ce4ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232196"
---
# <a name="troubleshoot-sales-quotations"></a>استكشاف أخطاء عروض أسعار المبيعات وإصلاحها

يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع عروض أسعار المبيعات.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>لا يمكنني تغيير كمية المبيعات لعرض أسعار المبيعات لصنف خدمة.

### <a name="issue-description"></a>وصف المشكلة

إذا حاولت تعيين كمية مبيعات (الحقل **SalesQty**) لصنف من النوع *خدمة* على بند عرض أسعار مبيعات، ستتلقى الرسالة التالية: "التحديث غير مسموح لحقل الكمية."

### <a name="issue-resolution"></a>حل المشكلة

لا يمكنك تعيين كمية مبيعات للمنتجات التي تعد أصناف خدمة. على سبيل المثال، إذا قمت بتقديم خدمة لتثبيت صنف، فلا يكون هذا الأمر منطقيًا لتسجيل كمية، بسبب عدم وجود صنف فعلي. توجد خدمة فقط.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]