---
title: تكوين منتج ليتم شراؤه مجانًا
description: يوضح هذا المقال كيفيه تكوين منتج بحيث يمكن شراؤه مجانا في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88370085de047a5e0be773dde218770cfa242d14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280354"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>تكوين منتج ليتم شراؤه مجانًا

[!include [banner](includes/banner.md)]


يوضح هذا المقال كيفيه تكوين منتج بحيث يمكن شراؤه مجانا في Microsoft Dynamics 365 Commerce.

## <a name="configure-the-product"></a>تكوين المنتج

لبيع منتج مجانا في Dynamics 365 Commerce ، يجب تعيين السعر الخاص به إلى 0 (صفر). بالاضافه إلى ذلك ، يجب ان تقوم بتكوين الاعداد **صالح سعر صفري** للمنتج.

لتكوين إعداد **صالح لسعر صفري** في المراكز الرئيسية للتجارة، اتبع هذه الخطوات.

1. انتقل إلى **‎البيع بالتجزئة والتجارة \> المنتجات والفئات \> المنتجات الصادرة حسب الفئة**.
1. انتقل إلى المنتج الذي ترغب في بيعه مجانا. 
1. في المقطع **التجارة** من الصفحة المنتج، قم بتعيين الخيار **صالح للسعر الصفري** إلى **نعم**.

يبين الرسم التوضيحي التالي مثالا لأحد المنتجات التي تم تعيين الخيار **صالح للسعر الصفري** الخاص بها إلى **نعم**.

![مثال لمنتج تم فيه تعيين الخيار الصالح لسعر الصفر إلى نعم.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>تكوين ملف تعريف وظائف المتجر عبر الإنترنت

قبل التمكن من معالجه الحركات المجانية ، يجب تكوين اعداد **السماح بالسحب بدون مدفوعات** لملف تعريف الوظائف الخاص بالمتجر الموجود علي الإنترنت بحيث يتم السماح بالحركات التي ليس لها مدفوعات. للحصول علي معلومات حول كيفيه إنشاء ملفات تعريف الوظائف ، راجع [إنشاء ملف تعريف الوظائف عبر الإنترنت](online-functionality-profile.md).

لتكوين إعداد **السماح بالسحب بدون مدفوعات** في المراكز الرئيسية للتجارة، اتبع هذه الخطوات.

1. انتقل إلى **Retail وCommerce \> إعداد القناة \> إعداد متجر على الإنترنت**.
1. في الصفحة الخاصة بملف تعريف وظائف المتجر ، ضمن **السحب** ، قم بتعيين خيار **السماح بالسحب بدون مدفوعات** إلى **نعم**.

يبين الرسم التوضيحي التالي مثالا لملف تعريف المتجر الفوري حيث يتم تعيين **خيار السماح بالسحب بدون مدفوعات** إلى **نعم**.

![مثال لملف تعريف المتجر الفوري حيث يتم تعيين خيار السماح بالسحب بدون مدفوعات إلى نعم.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>الموارد الإضافية

[إدارة أسعار مبيعات البيع بالتجزئة](price-management.md)

[إنشاء ملف تعريف وظائف على الإنترنت](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
