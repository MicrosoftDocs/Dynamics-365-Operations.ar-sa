---
title: تثبيت نسق Adventure Works
description: يصف هذا المقال كيفية تثبيت موضوع "أعمال المغامرة" في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: f5c195694633c96a473f0f824c1f182903082bff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274276"
---
# <a name="install-the-adventure-works-theme"></a>تثبيت نسق Adventure Works

[!include [banner](includes/banner.md)]

يصف هذا المقال كيفية تثبيت موضوع "أعمال المغامرة" في Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> ويتوفر نسق Adventure Works والوحدات النمطية اعتبارا من الإصدار 10.0.20 من Dynamics 365 Commerce. وهي متوفرة من Microsoft AppSource.

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل تثبيت سمة "أعمال المغامرة"، يجب أن يكون لديك بيئة Dynamics 365 Commerce (إصدار التجارة 10.0.20 أو أحدث) التي تتضمن Retail Cloud Scale Unit (RCSU) ومجموعة تطوير البرامج عبر الإنترنت التجارة (SDK) ومكتبة الوحدة النمطية التجارة. للحصول على معلومات حول كيفية تثبيت Commerce SDK ومكتبة الوحدة النمطية، راجع [‏‫إعداد بيئة تطوير‬](e-commerce-extensibility/setup-dev-environment.md). 

## <a name="installation-steps"></a>خطوات التثبيت

### <a name="install-the-adventure-works-theme-in-your-application"></a>تثبيت موضوع "أعمال المغامرة" في التطبيق الخاص بك

حزمة موضوع أعمال المغامرة متاحة في ملخص **dynamics365-commerce** ، كما **@msdyn365-commerce-theme/adventureworks-theme-kit**. ومع ذلك ، على الرغم من أن حزمة موضوع أعمال المغامرة هي جزء من هذا الموجز ، إلا أنها تحت مساحة اسم مختلفة. لذلك، يجب اتباع هذه الخطوات لإضافة إدخالات التسجيل لمساحة الاسم.

1. تحديث ملف **.npmrc** بحيث يتضمن إدخال التسجيل التالي (إذا لم يكن الإدخال مضمنا مسبقا):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. تحديث ملف **.yarnrc** بحيث يتضمن إدخال التسجيل التالي (إذا لم يكن الإدخال مضمنا مسبقا):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
لتثبيت الحزمة في البيئة المحلية الخاصة بك، قم بتشغيل الأمر `yarn add THEME_PACKAGE@VERSION` من موجه الأوامر، حيث **THEME_PACKAGE** هي حزمة الموضوع (@msdyn365-commerce-theme/adventureworks-theme-kit) و **VERSION** هو رقم إصدار مكتبه الوحدة النمطية المستخدم. من المهم أن يتم تطابق إصدارات حزمة الموضوع و مكتبة الوحدة النمطية. للعثور على رقم إصدار مكتبه الوحدة النمطية الصحيحة المراد استخدامه، افتح الملف package.json وحدد موقع القيمة **starter-pack** ضمن القسم **التبعيات**. في المثال التالي، يستخدم الملف package.json الإصدار 9.32 من مكتبة الوحدة النمطية التي يتم تعيينها إلى Dynamics 365 Commerce الإصدار 10.0.22.  

```json
"dependencies": {
    "@msdyn365-commerce-modules/starter-pack": "9.32",
}
```

يوضح المثال التالي كيفية تشغيل الأمر `yarn add` لإضافة الإصدار 9.32 من نسق Adventure Works‬. يقوم الأمر بتحديث ملف package.json تلقائيًا بحيث يتضمن التبعية.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit@9.32`

للحصول على المزيد من المعلومات حول كيفية تحديث إصدار مكتبة الوحدة الوطنية، راجع [تحديثات SDK ومكتبة الوحدات النمطية](e-commerce-extensibility/sdk-updates.md). 

> [!IMPORTANT]
> - يجب أن يتطابق إصدار السمة مع إصدار مكتبة الوحدة النمطية للتأكد من أن جميع الميزات تعمل كما هو متوقع. 
> - يجب أن يكون الإصدار الأدنى لمكتبة الوحدة النمطية التجارة SDK 10.0.20 (9.31). 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>إضافة ملفات الخط لموضوع "أعمال المغامرة"

بعد تثبيت سمة "أعمال المغامرة" في التطبيق الخاص بك، يجب إضافة ملفات الخط المطلوبة لذلك. لإكمال هذه الخطوة، نسخ كافة ملفات الخط من **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** إلى مسار الدليل العام للتطبيق الشريك **\public\webfonts**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>إعداد الموارد لموضوع "أعمال المغامرة"

الخطوة التالية هي تحديث المورد الافتراضي المطلوب للسمة. لإكمال هذه الخطوة، نسخ المحتوى من ملف global.json تحت **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** إلى ملف global.json لتطبيق الشريك تحت **\src\resources\modules**. إذا لم يكن الدليل الهدف **\src\resources** موجودا، يمكن نسخه بالكامل من الدليل المصدر **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** إلى الدليل الهدف **\src**.

### <a name="pull-updates-and-validate-the-theme"></a>سحب التحديثات والتحقق من صحة السمة

للحصول على معلومات حول كيفية سحب SDK أحدث مكتبة وحدة نمطية وتحديثات التبعية الأخرى راجع قسم "سحب التحديثات" من [SDK وتحديثات مكتبة الوحدة النمطية](e-commerce-extensibility/sdk-updates.md#pull-updates).

بعد أن يتم سحب تبعيات أحدث لأسفل، يمكنك تشغيل الأمر **بدء yarn** لبدء تشغيل ملقم العقدة في بيئة التطوير واختبار موضوع "أعمال المغامرة" الجديد. استعراض التطبيق محليا باستخدام معلمة سلسلة الاستعلام `?theme=adventureworks` (على سبيل المثال، `https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>الموارد الإضافية

[نسق أعمال المغامرة](adventure-works-theme.md)

[نظرة عامة على مكتبة الوحدات](starter-kit-overview.md)

[تحديثات SDK ومكتبة الوحدات](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
