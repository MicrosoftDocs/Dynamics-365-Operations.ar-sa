---
title: تسجيل الدفعات تلقائيًا لفواتير عميل أمر المبيعات بين الشركات الشقيقة
description: يشرح هذا الموضوع كيفية تسجيل الدفعات تلقائيًا لفواتير عميل أمر المبيعات بين الشركات الشقيقة
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
ms.openlocfilehash: ffc5c7bf44989fbcc18e940b5a7c9df81260d770
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548085"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>تسجيل الدفعات تلقائيًا لفواتير عميل أمر المبيعات بين الشركات الشقيقة

[!include [banner](../../includes/banner.md)]

ينشئ Microsoft Dynamics 365 Supply Chain Management حركة عميل عند ترحيل فاتورة عميل بين الشركات الشقيقة. تبقى حركة العميل هذه مفتوحة حتى تتم تسويتها، مما يعني أنه تم تسديدها. عند تحديث فاتورة أمر الشراء المناظر بين الشركات الشقيقة، يتم إنشاء حركة مورّد تتطابق مع حركة العميل. تبقى حركة المورّد هذه مفتوحة أيضًا إلى أن تتم تسويتها. لتقليل خطر اختلافات، يمكن إنشاء دفتر يومية دفعات الحسابات المدينة وترحيله بشكل تلقائي عند ترحيل دفتر يومية دفعات الحسابات الدائنة.

1. انتقل إلى **المبيعات والتسويق \> العملاء \> جميع العملاء‬**.
1. في جزء "الإجراءات"، على علامة تبويب **عام**، حدد **بين شركات شقيقة**.
1. لإعداد دفعات الحسابات المدينة بين الشركات الشقيقة في الصفحة **بين شركات شقيقة** لأوامر المبيعات، حدد الارتباط **سياسات أوامر المبيعات**.
1. في الحقل **الحقل دفتر يومية المدفوعات**، حدد دفتر يومية مدفوعات الحسابات المدينة الذي ترغب في تسجيل دفعات المورّد بين الشركات الشقيقة له. يمكنك إعداد ذلك في صفحة **معلمات الحسابات المدينة**.
1. إذا أردت الترحيل إلى دفتر اليومية هذا تلقائيًا، فحدد خانة الاختيار **ترحيل دفتر اليومية تلقائيًا**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
