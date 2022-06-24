---
title: استيراد كتالوجات المورِّد
description: يصف هذا المقال عملية استيراد بيانات كتالوج المورد.
author: GalynaFedorova
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gfedorova
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 19fa26eeb8ea3c0944be199c57eaf4a2d7e76034
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851612"
---
# <a name="import-vendor-catalogs"></a>استيراد كتالوجات المورِّد

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>استيراد كتالوجات المورِّد

في Dynamics 365 Supply Chain Management، بإمكان محترفي الشراء إنشاء وصيانة كتالوجات يمكن لموظفي الشركة استخدامها عندما يطلبون الأصناف والخدمات للاستخدام الداخلي. لإنشاء كتالوج تدبير، يمكنك إضافة الأصناف والخدمات التي تريد توفيرها للموظفين، إما عن طريق استيراد بيانات كتالوج المنتج أو عن طريق إضافة بيانات كتالوج المنتج لأصل المنتج يدوياً. 

يمكنك تحميل بيانات الكتالوج المرسلة من قِبل مورّد من عميل Microsoft Dynamics 365.

يجب أن تكون بيانات المنتج التي يرسلها مورد إليك، بصيغة ملف طلب كتالوج (CMR)، بتنسيق ملف XML. يجب أن يحتوي ملف CMR على تفاصيل المنتجات التي يوفرها المورد لشركتك.

## <a name="import-vendor-catalog-data"></a>استيراد بيانات كتالوج المورِّد

لاستيراد كتالوج المورّد، يجب أن تكمل المهام التالية:

1. إعداد مشروع في مساحة عمل إدارة البيانات حيث قمت بتحديد قواعد تعيين البيانات الخاصة بك. حدد **إدارة البيانات**، ثم حدد **إعداد أدوار لمشاريع البيانات**.

2. إعداد تدرج هرمي لفئات التدبير، وقم بتعيين الموردين لفئات التدبير. إذا كنت تستخدم أكواد السلع، فقم بإضافة أكواد السلع إلى فئات التدبير. لمزيد من المعلومات حول إعداد تدرج هرمي لفئات التدبير، راجع [إعداد تدرج هرمي لفئات التدبير](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3. تكوين بيانات المورّد لاستيراد الكتالوج. حدد موردًا، ثم حدد **التدبير** > **إعداد** > **تكوين المورد لاستيراد الكتالوج**.

4. تكوين سير العمل لاستيراد الكتالوج. أنشئ قالب ملف CMR وشارك هذا مع المورد الخاص بك.

5. حدد **التدبير والتوريد**\>**الشائعة**\>**الكتالوجات**\>**كتالوجات الموردين** لإنشاء كتالوج مورد. يتم تجميع ملفات طلب صيانة الكتالوج (CMR) التي تتلقاها من المورد الخاص بك في هذا الكتالوج. 

6. تحميل ملف CMR.

7. قم بمراجعة أو اعتماد أو رفض المنتجات في كتالوج المورد. يتم تعيين المنتجات بشكل تلقائي إلى فئات التدبير. 

وتتم إضافة المنتجات المعتمدة إلى أصول المنتجات ويتم إصدارها إلى الكيانات القانونية المحددة، أو يمكن استخدامها لإنشاء أوامر شراء. يمكن إضافة المنتجات المدعومة فقط إلى كتالوج التدبير.

## <a name="generate-a-catalog-import-file-template"></a>إنشاء قالب ملف استيراد كتالوج

يتألف قالب ملف استيراد الكتالوج من ملف XSD الذي تستخدمه لإنشاء ملف طلب صيانة الكتالوج لمنتجات المورّد. يمكنك استخدام ملف طلب صيانة الكتالوج لإنشاء كتالوج جديد، أو استبدال كتالوج حالي، أو تعديل كتالوج حالي.

1. حدد **التدبير والتوريد** \> **الكتالوجات** \> **كتالوجات الموردين** وانقر نقراً مزدوجاً فوق الكتالوج الذي تريد العمل فيه.

2. تنزيل قالب استيراد كتالوج حالي (ملف XSD). في صفحة **تحديث الكتالوج**، في **جزء الإجراءات**، في علامة التبويب **الكتالوجات**، في مجموعة **المعلومات ذات الصلة**، انقر فوق **إنشاء قالب كتالوج**، ثم حدد **فئة التدبير**.

    - باستخدام خيار **فئة التدبير**، يمكنك إنشاء قالب الكتالوج الذي يحتوي على فئات التدبير التي يتم فيها اعتماد المورد لتقديم المنتجات.

3. في مربع الحوار **حفظ باسم**، حدد الموقع الذي تريد تخزين قالب ملف الكتالوج، وحفظ الملف به.

لمزيد من المعلومات والأمثلة، ارجع إلى نشرة المدونة هذه: [كتالوجات الموردين في Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]