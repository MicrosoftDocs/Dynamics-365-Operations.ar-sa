---
title: استيراد التقييمات والمراجعات وتصديرها
description: يوضح هذا الموضوع كيفية استيراد تقييمات المنتجات ومراجعاتها وتصديرها في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 3ae85f21f7a78d56621aed60527207badcee9c75
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968505"
---
# <a name="import-and-export-ratings-and-reviews"></a>استيراد التقييمات والمراجعات وتصديرها

[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية استيراد تقييمات المنتجات ومراجعاتها وتصديرها في Microsoft Dynamics 365 Commerce.

يقدم Dynamics 365 Commerce [تقييمات ومراجعات](ratings-reviews-overview.md) كحل للقناة متعددة الاتجاهات. عندما تقوم بالتبديل إلى حل التقييمات والمراجعات في Dynamics 365 Commerce، قد ترغب في نقل بيانات التقييمات والمراجعات الموجودة إلى النظام الأساسي Commerce. وقد ترغب أيضًا في تصدير بيانات التقييمات والمراجعات من Commerce، بالاستناد إلى متطلبات العمل. يسمح لك موصل Power Automate باستيراد التقييمات والمراجعات إلى Commerce وتصديرها من Commerce.

> [!NOTE]
> للحصول على معلومات حول كيفيه الشروع في العمل مع عمليات سير العمل المنطقية في Power Automate، راجع [إنشاء سير عمل سحابي في Power Automate](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل أن تتمكن من استيراد التقييمات والمراجعات وتصديرها، يجب عليك الوفاء بالمتطلبات الأساسية التالية:

- يجب تمكين حل التقييمات والمراجعات لموقع التجارة الإلكترونية على النظام الأساسي Commerce. لمزيد من المعلومات، راجع [الموافقة على استخدام التقييمات والمراجعات](opt-in-ratings-reviews.md).
- يجب تكوين موصل Power App للمراجعات والتقييمات في Dynamics 365 لتمكين إجراءات "إرسال المراجعات" أو "تصدير المراجعات" في Power Automate. لمزيد من المعلومات، راجع [Dynamics 365 Commerce - التقييمات والمراجعات (إصدار أولي)](/connectors/dynamics365ratingsre/).
- يجب تكوين المصادقة من خدمة إلى خدمة (S2S) لاستدعاء واجهة برمجة التطبيقات للتقييمات والمراجعات من خارج Commerce بطريقة آمنة. لمزيد من المعلومات، راجع [تكوين مصادقة من خدمة إلى خدمة‬](service-to-service-auth.md).

## <a name="import-ratings-and-reviews"></a>استيراد التقييمات والمراجعات

لاستيراد التقييمات والمراجعات من نظامك الموجود إلى Commerce، يجب إضافة موصل Power Automate للمراجعات والتقييمات في Dynamics 365 إما إلى سير عمل Power Automate موجود أو سير عمل جديد. لمزيد من المعلومات، راجع [Dynamics 365 Commerce - التقييمات والمراجعات (إصدار أولي)](/connectors/dynamics365ratingsre/).

> [!IMPORTANT]
> قبل أن تتمكن من إكمال هذا الإجراء، يجب [تكوين مصادقة S2S](service-to-service-auth.md).

لاستيراد التقييمات والمراجعات إلى Commerce باستخدام موصل Power Automate للتقييمات والمراجعات في Dynamics 365، اتبع الخطوات التالية.

1. حدد الإجراء **إرسال مراجعة المستخدم**.
1. أنشئ اتصالاً باستخدام معلومات تطبيق Azure Active Directory (Azure AD) التي تم إنشاؤها عندما قمت بتكوين مصادقة S2S. لمزيد من المعلومات، راجع [تكوين مصادقة من خدمة إلى خدمة‬](service-to-service-auth.md).
1. يأخذ الإجراء **إرسال مراجعة المستخدم** كل مراجعة على حدة. وبالتالي، كرر الإجراء. استخدم المراجعات المصدر كقائمة لإرسال مراجعات مجمعة.
    
## <a name="export-ratings-and-reviews"></a>تصدير التقييمات والمراجعات

لتصدير التقييمات والمراجعات من Commerce، يجب إضافة موصل Power Automate للمراجعات والتقييمات في Dynamics 365 إما إلى سير عمل Power Automate موجود أو سير عمل جديد. لمزيد من المعلومات، راجع [Dynamics 365 Commerce - التقييمات والمراجعات (إصدار أولي)](/connectors/dynamics365ratingsre/).

لتصدير التقييمات والمراجعات من Commerce باستخدام موصل Power Automate للتقييمات والمراجعات في Dynamics 365، اتبع الخطوات التالية.

1. حدد الإجراء **تصدير جميع المراجعات**.
1. أكمل الإجراء. 

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على التقييمات والمراجعات](ratings-reviews-overview.md)

[الموافقة على استخدام التقييمات والمراجعات](opt-in-ratings-reviews.md)

[إدارة التقييمات والمراجعات](manage-reviews.md)

[تكوين التقييمات والمراجعات](configure-ratings-reviews.md)

[مزامنة تقييمات المنتجات](sync-product-ratings.md)

[تمكين النشر اليدوي لتقييمات ومراجعات بواسطة المشرف](manual-publish-rating-reviews.md)

[تكوين مصادقة من خدمة إلى خدمة](service-to-service-auth.md)

[الأسئلة المتداولة حول التقييمات والمراجعات](ratings-reviews-faq.md)
