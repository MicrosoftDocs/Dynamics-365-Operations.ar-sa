---
title: الموافقة على استخدام التقييمات والمراجعات
description: يشرح هذا الموضوع كيفية الاشتراك في استخدام التقييمات والمراجعات في موقع Microsoft Dynamics 365 Commerce .
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 481a8750b2333d5dd5de2c05e175569804a6046f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985826"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>الموافقة على استخدام التقييمات والمراجعات

[!include [banner](includes/banner.md)]

يشرح هذا الموضوع كيفية الاشتراك في استخدام التقييمات والمراجعات في موقع Microsoft Dynamics 365 Commerce .

## <a name="overview"></a>نظرة عامة

حل التقييمات والمراجعات هو حل متعدد الاتجاهات يمكنك توفيره في Dynamics 365 Commerce باستخدام Microsoft Dynamics Lifecycle Services (LCS). LCS هو مدخل للإدارة يستخدمه بائعو التجزئة لإدارة بيئاتهم بداية من التشغيل وحتى التفكيك.

إذا كنت ترغب في استخدام حل التصنيفات والمراجعات علي موقع ويب الخاص بالتجارة ، فيجب عليك الاشتراك في التصنيفات والمراجعات اثناء نشر موقع التجارة الكترونيه على Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>الموافقة على استخدام التقييمات والمراجعات

للاشتراك في استخدام التقييمات والمراجعات على موقعك، اتبع الخطوات التالية.

1. اتبع الخطوات في [‏‫نشر موقع تجارة إلكترونية جديد‬](deploy-ecommerce-site.md)
1. بينما تكون في LCS، انتقل إلى **‏‫إعداد نشر Retail‬ \> إعدادات أخرى**.
1. قم بتعيين خيار **تمكين خدمة التقييمات والمراجعات** إلى **نعم**.
1. في الحقل **مجموعه أمان AAD الخاصة بالمشرف على التقييمات والمراجعات (معرف كائن مجموعة الأمان)**، أدخل معرف مجموعة أمان Microsoft Azure Active Directory (Azure AD) التي تتضمن المشرفين على التقييمات والمراجعات.

    ![الموافقة على استخدام التقييمات والمراجعات](media/LCS_RnR_Preference.png)

1. أكمل عملية تهيئة التجارة الإلكترونية.

> [!NOTE] 
> إذا كنت عميلا حاليًا لـ Dynamics 365 Commerceقد قام بالفعل بنشر موقع تجاره الكترونيه دون ان يتم الاشتراك في التصنيفات والمراجعات وترغب الآن في استخدام التصنيفات والمراجعات من حزمة Dynamics 365 Commerce، فالرجاء تقديم طلب خدمه. لمزيد من المعلومات حول كيفيه تقديم طلب خدمه، راجع [عملية إرسال الطلبات](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على التقييمات والمراجعات](ratings-reviews-overview.md)

[إدارة التقييمات والمراجعات](manage-reviews.md)

[تكوين التقييمات والمراجعات](configure-ratings-reviews.md)

[مزامنة تقييمات المنتجات في Dynamics 365 Commerce](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]