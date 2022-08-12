---
title: استكشاف مشكلات ملحق Store Commerce وإصلاحها
description: يوضح هذا المقال كيفيه استكشاف مشكلات الملحق وإصلاحها في تطبيق Store Commerce Microsoft Dynamics 365 Commerce.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b440183e255e05c4f93a4f11106be2967163ff74
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169007"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>استكشاف مشكلات ملحق Store Commerce وإصلاحها

[!include [banner](../includes/banner.md)]

يوضح هذا المقال كيفيه استكشاف مشكلات الملحق وإصلاحها في تطبيق Store Commerce Microsoft Dynamics 365 Commerce.

## <a name="extensions-packages-arent-loaded"></a>لم يتم تحميل حزم الملحقات

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>عدم ظهور حزم الملحقات علي صفحه إعدادات POS \>

ربما لم يتم تحديث Commerce runtimeCRTالتجارية لتضمين حزمه الملحق ، أو انها لا يتم نشرها. لمزيد من المعلومات ، راجع [Commerce runtime (CRT) القابلة للتوسعة](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>تظهر حزم الملحقات في الصفحة إعدادات نقطه البيع \> ، لكن لم يتم تحميل ملف البيان

تاكد من وجود حزم الملحقات في المجلد **C:\\Program Files\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Extensions** . إذا كانت الحزم موجودة ، يجب ان يكون **هناك مجلد نقطه POS** الذي يحتوي علي البيان.

إذا لم **يكن هناك مجلد نقطه POS** ، فتاكد من ان مشروع Store Commerceيشير إلى مشروع العملية الملحقة لنقطه البيع (POS) بشكل صحيح. قم بالتحقق من صحة مسار مرجع المشروع ، وتاكد من وجوده. 

في المثال التوضيحي التالي ، مشروع المثبت يواجه مشكلات مع مشروع الملحق المشار اليه.

![مرجع Store Commerce غير صالح.](media/ReferenceNotValid.png)

إذا تمت أضافه مرجع المشروع الملحق بشكل صحيح ، لن يكون هناك اي مشكله تحذير أو مشكله تبعية في مشروع المثبت ، كما هو موضح في المثال التالي من الرسم التوضيحي.

![مرجع مشروع Store Commerce غير صالح.](media/ReferenceValid.png)
