---
title: استكشاف أخطاء عروض أسعار المبيعات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع عروض أسعار المبيعات.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 92b77c1b7de1f5c946e677c810c0d0e43427473e7ba26679df23f7663946dbc0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765384"
---
# <a name="troubleshoot-sales-quotations"></a>استكشاف أخطاء عروض أسعار المبيعات وإصلاحها

يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع عروض أسعار المبيعات.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>لا يمكنني تغيير كمية المبيعات لعرض أسعار المبيعات لصنف خدمة.

### <a name="issue-description"></a>وصف المشكلة

إذا حاولت تعيين كمية مبيعات (الحقل **SalesQty**) لصنف من النوع *خدمة* على بند عرض أسعار مبيعات، ستتلقى الرسالة التالية: "التحديث غير مسموح لحقل الكمية."

### <a name="issue-resolution"></a>حل المشكلة

لا يمكنك تعيين كمية مبيعات للمنتجات التي تعد أصناف خدمة. على سبيل المثال، إذا قمت بتقديم خدمة لتثبيت صنف، فلا يكون هذا الأمر منطقيًا لتسجيل كمية، بسبب عدم وجود صنف فعلي. توجد خدمة فقط.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]