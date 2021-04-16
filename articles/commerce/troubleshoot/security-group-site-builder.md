---
title: لا يمكن تكوين مجموعة أمان لمنشئ موقع التجارة أثناء النشر الأولي
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور مجموعة أمان Microsoft Azure Active Directory (Azure AD) لمنشئ موقع التجارة كخيار عند إنشاء مكونات التجارة الإلكترونية في Microsoft Dynamics Lifecycle Services (LCS) أثناء النشر الأولي لمستأجر التجارة الإلكترونية الجديد.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: aa00e9331693600ced2f4ead399a0c005b77ad08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801497"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>لا يمكن تكوين مجموعة أمان لمنشئ موقع التجارة أثناء النشر الأولي

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور مجموعة أمان Microsoft Azure Active Directory (Azure AD) لمنشئ موقع التجارة كخيار عند إنشاء مكونات التجارة الإلكترونية في Microsoft Dynamics Lifecycle Services (LCS) أثناء النشر الأولي لمستأجر التجارة الإلكترونية الجديد.

## <a name="description"></a>الوصف

عند إنشاء مكونات التجارة الإلكترونية كجزء من عملية نشر مستأجر التجارة الإلكترونية الجديد التي تشتمل على مكون منشئ موقع التجارة، فإن مجموعة أمان Azure AD لا تظهر كخيار في مربع الحوار.

## <a name="resolution"></a>الدقة

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>توفير موقع التجارة الإلكترونية مع مستخدم في المستأجر الصحيح

1. انتقل إلى [مدخل Azure](https://portal.azure.com/).
1. تحت المستأجر تم توفير مشروع LCS لموقع التجارة الإلكترونية له، اتبع الإرشادات الموجودة في [إنشاء مجموعة أساسية وأضف الأعضاء باستخدام Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. انتقل إلى [LCS](https://lcs.dynamics.com/)، وقم بتسجيل الدخول باستخدام حساب يشترك في نفس المستأجر مثل مجموع أمان Azure AD التي قمت بإنشائها. يجب أن يكون للحساب حق الوصول لعرض مجموعة أمان Azure AD.
1. قم بإكمال خطوات الإعداد لتكوين موقع التجارة الإلكترونية. عندما تقوم بتوفير مكونات التجارة الإلكترونية، يجب أن تظهر الآن مجموعة الأمان كخيار في مربع الحوار.

> [!NOTE]
> لضمان ملء الحقل في مربع الحوار بقائمة مجموعات الأمان، يجب عليك تحديد **إدخال** بعد إدخال اسم مجمةعة أمان Azure AD التي قمت بإنشائها. ستسرد نتائج البحث كافة مجموعات أمان Azure AD التي تبدأ بنص البحث، ويمكن للمستخدم الوصول إليها. يمكنك استخدام مصطلح بحث أقصر للسماح بنتائج بحث أوسع.

## <a name="additional-resources"></a>الموارد الإضافية

[إنشاء مجموعة أساسية وإضافة الأعضاء باستخدام Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[نشر مستأجر تجارة إلكترونية جديد](../deploy-ecommerce-site.md)
