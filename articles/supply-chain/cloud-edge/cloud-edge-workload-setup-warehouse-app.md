---
title: تكوين تطبيق الأجهزة المحمولة Warehouse Management لوحدات قياس السحابة والحافة
description: يوضح هذا المقال كيفية إعداد تطبيق الأجهزة المحمولة Warehouse Management للمستودعات التي تتلقى خدمات وحدة قياس السحابة أو الحافة.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865227"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>تكوين تطبيق الأجهزة المحمولة Warehouse Management لوحدات قياس السحابة والحافة

[!include [banner](../includes/banner.md)]

يوضح هذا المقال كيفية إعداد تطبيقات الأجهزة المحمولة Warehouse Management كي يتم استخدامها في المستودعات التي تتلقى خدمات وحدة قياس السحابة أو الحافة.

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل البدء في إعداد أجهزتك المحمولة للاتصال بوحدة قياس السحابة أو الحافة، تأكد من أنها قادرة على الاتصال بمركز المؤسسة. للحصول على الإرشادات، راجع [تثبيت وتكوين تطبيق الأجهزة المحمولة Warehouse Management](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>إعداد إضافي عند تشغيل تطبيق الأجهزة المحمولة Warehouse Management مقابل وحدة قياس

وكجزء من [عملية نشر أحمال عمل وحدة قياس المستودع](cloud-edge-landing-page.md#scale-unit-manager-portal)، تتم مزامنة معظم البيانات المطلوبة لتوصيل أجهزة تطبيق الأجهزة المحمولة Warehouse Management بشكل تلقائي من مركز المؤسسة إلى وحدة القياس. ومع ذلك، يجب إدخال البيانات في صفحة **تطبيقات Azure Active Directory** (**إدارة النظام \> الإعداد \> تطبيقات Azure Active Directory**) في عملية نشر وحدة القياس. علاوةً على ذلك، قد تحتاج إلى تحديث قيمة **الشركة** الافتراضية لمعرف المستخدم أو إنشاء مستخدم جديد. لن يتمكن المستخدمون المرتبطون بشركة غير موجودة في نشر وحدة قياس من تسجيل الدخول عند توصيل تطبيق الأجهزة المحمولة Warehouse Management بوحدة القياس هذه.

> [!NOTE]
> نظرًا لعدم مزامنة البينات الموجودة في صفحة **تطبيقات Azure Active Directory**، يجب عليك الاحتفاظ بهذه البيانات يدويًا إذا كنت تريد نقل أحمال عمل المستودع إلى وحدة قياس أخرى.

تذكر أنه كجزء من إعداد الاتصال لكل تطبيق أجهزة محمولة Warehouse Management، يجب أن يكون عنوان URL لمورد Azure Active Directory المحدد لوحدة القياس بدلاً من مركز المؤسسة.
