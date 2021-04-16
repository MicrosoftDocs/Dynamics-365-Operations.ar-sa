---
title: استكشاف أخطاء عمل المستودع وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمل المستودعات في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 08cc074fe851b952ebfc942ae3d1cb05240d3b91
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837429"
---
# <a name="troubleshoot-warehouse-work"></a>استكشاف أخطاء عمل المستودع وإصلاحها

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمل المستودعات في Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>لا يمكن نقل لوحات الترخيص التي تحتوي علي أصناف أرقام تسلسليه عند السماح بإصدار فارغ وإيصال فارغ في مجموعه ابعاد التعقب.

### <a name="issue-description"></a>وصف المشكلة

لا يمكنك نقل لوحه ترخيص باستخدام عنصر قائمه **الحركة** إذا كان الرقم المسلسل يحتوي علي إعدادات *لإصدار فارغ مسموح به* و *تم السماح بإيصال فارغ* في مجموعه بعد التعقب، وإذا كان هناك عده لوحات ترخيص في نفس الموقع ، يكون لبعضها الأرقام التسلسلية وبعضها لا تملكها.

### <a name="issue-resolution"></a>حل المشكلة

سيتم حل هذه المشكلة من خلال التغييرات التي يتم نشرها في [قاعدة المعارف 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). ستؤدي هذه التغييرات إلى جعل حقل **الرقم التسلسلي** اختياريا عند السماح بالاستلام الفارغ والإصدار الفارغ.

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>أتلقى رسالة الخطا التالية في تطبيق إدارة المستودع للأجهزة المحمولة عند معالجه الحركات: "مالك المخزون غير %1مسموح به في هذه العملية."

### <a name="issue-description"></a>وصف المشكلة

بعد تتبع **المالك** لا يكون موجودا عند استخدام تطبيق إدارة المستودع للأجهزة المحمولة لعمل الحركات. يظهر دفتر يوميه تحويل المخزون العادي من عميل Supply Chain Management للعمل كما يجب ولا يمكن ترحيله الا إذا تم ملء بعد **المالك**.

### <a name="issue-resolution"></a>حل المشكلة

قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه. تدعم عمليات أداره المستودع حاليا المخزون الذي يملكه الكيان القانوني فقط.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]