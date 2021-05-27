---
title: لا يمكن تكوين مجموعة أمان لمنشئ موقع التجارة أثناء النشر الأولي
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور مجموعة أمان Microsoft Azure Active Directory (Azure AD) لمنشئ موقع التجارة كخيار عند إنشاء مكونات التجارة الإلكترونية في Microsoft Dynamics Lifecycle Services (LCS) أثناء النشر الأولي لمستأجر التجارة الإلكترونية الجديد.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: d29e560d0f7b2bbc2415d7a0f6fe18f2ca17dc7c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020722"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>لا يمكن تكوين مجموعة أمان لمنشئ موقع التجارة أثناء النشر الأولي

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور مجموعة أمان Microsoft Azure Active Directory (Azure AD) لمنشئ موقع التجارة كخيار عند إنشاء مكونات التجارة الإلكترونية في Microsoft Dynamics Lifecycle Services (LCS) أثناء النشر الأولي لمستأجر التجارة الإلكترونية الجديد.

## <a name="description"></a>الوصف

عند إنشاء مكونات التجارة الإلكترونية كجزء من عملية نشر مستأجر التجارة الإلكترونية الجديد التي تشتمل على مكون منشئ موقع التجارة، فإن مجموعة أمان Azure AD لا تظهر كخيار في مربع الحوار.

## <a name="resolution"></a>الدقة

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>توفير موقع التجارة الإلكترونية مع مستخدم في المستأجر الصحيح

1. انتقل إلى [مدخل Azure](https://portal.azure.com/).
1. تحت المستأجر تم توفير مشروع LCS لموقع التجارة الإلكترونية له، اتبع الإرشادات الموجودة في [إنشاء مجموعة أساسية وأضف الأعضاء باستخدام Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. انتقل إلى [LCS](https://lcs.dynamics.com/)، وقم بتسجيل الدخول باستخدام حساب يشترك في نفس المستأجر مثل مجموع أمان Azure AD التي قمت بإنشائها. يجب أن يكون للحساب حق الوصول لعرض مجموعة أمان Azure AD.
1. قم بإكمال خطوات الإعداد لتكوين موقع التجارة الإلكترونية. عندما تقوم بتوفير مكونات التجارة الإلكترونية، يجب أن تظهر الآن مجموعة الأمان كخيار في مربع الحوار.

> [!NOTE]
> لضمان ملء الحقل في مربع الحوار بقائمة مجموعات الأمان، يجب عليك تحديد **إدخال** بعد إدخال اسم مجمةعة أمان Azure AD التي قمت بإنشائها. ستسرد نتائج البحث كافة مجموعات أمان Azure AD التي تبدأ بنص البحث، ويمكن للمستخدم الوصول إليها. يمكنك استخدام مصطلح بحث أقصر للسماح بنتائج بحث أوسع.

## <a name="additional-resources"></a>الموارد الإضافية

[إنشاء مجموعة أساسية وإضافة الأعضاء باستخدام Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[نشر مستأجر تجارة إلكترونية جديد](../deploy-ecommerce-site.md)