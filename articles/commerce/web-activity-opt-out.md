---
title: إلغاء الاشتراك من مجموعة أحداث نشاط الويب
description: يشرح هذا الموضوع كيفية السماح لزوار موقع ويب الخاص بك بإلغاء الاشتراك من مجموعة أحداث نشاط الويب في Microsoft Dynamics 365 Commerce.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b0e48307527a8fea729d8dfdcdbc6337be0faf1
ms.sourcegitcommit: 8058db089b8768076ff1250be77d42a6e2b3f570
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378982"
---
# <a name="opt-out-of-web-activity-event-collection"></a>إلغاء الاشتراك من مجموعة أحداث نشاط الويب
[!include [banner](includes/banner.md)]

يشرح هذا الموضوع كيفية السماح للعملاء بإلغاء الاشتراك من مجموعة أحداث نشاط الويب في Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

يتيح Dynamics 365 Commerce لمسؤولي المواقع تحليل نشاط الويب لمستخدمي مواقع التجارة الإلكترونية الخاصة بهم. وبهذه الطريقة، يمكنهم فهم كيف يتم استخدام مواقعهم بشكل أفضل، كما يمكنهم تحسين المواقع لتوفير تجربة مستخدم محسنة وتلبية أهداف الأعمال.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>طرق للمسؤولين لتنفيذ تجربة إلغاء الاشتراك

يتوفر للمسؤولين ثلاث طرق لتنفيذ تجربة إلغاء الاشتراك.

### <a name="opt-out-on-behalf-of-users"></a>إلغاء الاشتراك نيابةً عن المستخدمين

في إدارة الحسابات في Commerce headquarters (HQ)، يمكن للمسؤولين إلغاء الاشتراك بالنيابة عن المستخدمين.

1. في عميل HQ ، في صفحة **كافة العملاء**، ابحث عن عميل وحدده.
1. من الصفحة تفاصيل العميل، في علامة التبويب السريعة **البيع بالتجزئة**، في قسم **الخصوصية**، قم بتعيين خيار **عدم تعقب نشاط الويب** إلى **نعم**.

    ![إعدادات الخصوصية](media/Disablepersonalizationpart2.png)

1. حدد **حفظ** ثم قم بإغلاق الصفحة.

### <a name="module-based-opt-out-experience"></a>تجربه إلغاء الاشتراك المستند إلى الوحدة النمطية

يمكن للمسؤولين السماح للمستخدمين المصادق عليهم بإلغاء الاشتراك من مجموعة أحداث نشاط الويب بأنفسهم. لتوفير تجربه إلغاء الاشتراك هذه ، أضف الوحدة النمطية للغاء اشتراك المستخدم إلى صفحات ملف تعريف حساب العميل.

### <a name="custom-extensions"></a>الملحقات المخصصة

يمكن للمسؤولين إنشاء الملحقات الخاصة بهم لإدارة تجربة إلغاء الاشتراك للمستخدمين. لمزيد من المعلومات، راجع [استدعاء واجهات برمجة تطبيقات Retail Server](e-commerce-extensibility/call-retail-server-apis.md) و[توسعة القنوات على الإنترنت](e-commerce-extensibility/overview.md).