---
title: إلغاء الاشتراك من مجموعة أحداث نشاط الويب
description: يشرح هذا المقال كيفية السماح لزوار موقع ويب الخاص بك بإلغاء الاشتراك من مجموعة أحداث نشاط الويب في Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 81343f5033366484140f73fcc313ecd9f35e7d47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286715"
---
# <a name="opt-out-of-web-activity-event-collection"></a>إلغاء الاشتراك من مجموعة أحداث نشاط الويب
[!include [banner](includes/banner.md)]

يشرح هذا المقال كيفية السماح للعملاء بإلغاء الاشتراك من مجموعة أحداث نشاط الويب في Microsoft Dynamics 365 Commerce.

يتيح Dynamics 365 Commerce لمسؤولي المواقع تحليل نشاط الويب لمستخدمي مواقع التجارة الإلكترونية الخاصة بهم. وبهذه الطريقة، يمكنهم فهم كيف يتم استخدام مواقعهم بشكل أفضل، كما يمكنهم تحسين المواقع لتوفير تجربة مستخدم محسنة وتلبية أهداف الأعمال.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>طرق للمسؤولين لتنفيذ تجربة إلغاء الاشتراك

يتوفر للمسؤولين ثلاث طرق لتنفيذ تجربة إلغاء الاشتراك.

### <a name="opt-out-on-behalf-of-users"></a>إلغاء الاشتراك نيابةً عن المستخدمين

في إدارة الحسابات في Commerce headquarters (HQ)، يمكن للمسؤولين إلغاء الاشتراك بالنيابة عن المستخدمين.

1. في عميل HQ ، في صفحة **كافة العملاء**، ابحث عن عميل وحدده.
1. من الصفحة تفاصيل العميل، في علامة التبويب السريعة **البيع بالتجزئة**، في قسم **الخصوصية**، قم بتعيين خيار **عدم تعقب نشاط الويب** إلى **نعم**.

    ![إعدادات الخصوصية.](media/Disablepersonalizationpart2.png)

1. حدد **حفظ** ثم قم بإغلاق الصفحة.

### <a name="module-based-opt-out-experience"></a>تجربه إلغاء الاشتراك المستند إلى الوحدة النمطية

يمكن للمسؤولين السماح للمستخدمين المصادق عليهم بإلغاء الاشتراك من مجموعة أحداث نشاط الويب بأنفسهم. لتوفير تجربه إلغاء الاشتراك هذه ، أضف الوحدة النمطية للغاء اشتراك المستخدم إلى صفحات ملف تعريف حساب العميل.

### <a name="custom-extensions"></a>الملحقات المخصصة

يمكن للمسؤولين إنشاء الملحقات الخاصة بهم لإدارة تجربة إلغاء الاشتراك للمستخدمين. لمزيد من المعلومات، راجع [استدعاء واجهات برمجة تطبيقات Retail Server](e-commerce-extensibility/call-retail-server-apis.md) و[توسعة القنوات على الإنترنت](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
