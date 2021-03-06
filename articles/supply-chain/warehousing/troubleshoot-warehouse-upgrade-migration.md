---
title: استكشاف أخطاء الترقية والترحيل إلى الإدارة المتقدمة للمستودع وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء الترقية والترحيل إلى إدارة المستودعات المتقدمة.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993848"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>استكشاف أخطاء الترقية والترحيل إلى الإدارة المتقدمة للمستودع وإصلاحها

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء الترقية والترحيل إلى إدارة المستودعات المتقدمة.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>أتلقى رسالة الخطا التالية: "java.security.cert.certPathValidatorException: لم يتم العثور علي الثقة التي تم ربطها لمسار الشهادة."

### <a name="issue-description"></a>وصف المشكلة

تظهر رسالة الخطا هذه في تطبيق المستودع ، وذلك لان الشهادات الموقعة ذاتيا غير موثوق بها في Android 8+ في البيئات المحلية.

### <a name="issue-resolution"></a>حل المشكلة

استخدم المرجع المصدق (العام) الخارجي (CA). يتوفر إصلاح لهذه المشكلة في إصدار 1.9.0.0 تطبيق المستودع. لمزيد من المعلومات حول هذه المشكلة وكيفيه حلها ، راجع [استكشاف مشكلات الاتصال بتطبيق المستودع وإصلاحها](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>ما هي العملية المعتمدة للتنقل من التخزين الأساسي إلى التخزين المتقدم؟

### <a name="issue-description"></a>وصف المشكلة

أنت تعمل حاليا ضمن أداره المخزون/المخزون وباستخدام وظيفة الأسهم الاساسيه ، وتريد الانتقال إلى التخزين المتقدم للاستفادة من الاجهزه المحمولة والأمواج والعمل. ومع ذلك ، تواجه مشكلات عند محاولة القيام بهذا النقل. علي سبيل المثال ، لا يمكنك تغيير منتجاتك بحيث تستخدم ابعاد التخزين (الموقع والمستودع والموقع) ، نظرا لان المنتجات تحتوي علي حركات مقابله. لذلك، يجب أن تتعلم العملية المعتمدة للتنقل من التخزين الأساسي إلى التخزين المتقدم.

### <a name="issue-resolution"></a>حل المشكلة

لمزيد من المعلومات حول عمليه النقل من التخزين الأساسي إلى التخزين المتقدم ، راجع النشرات الخاصة بالمدونة والوثائق:

- [تمكين عملية إدارة المستودعات للأصناف والمستودعات الموجودة](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [ترحيل Microsoft Dynamics AX WMS إلى مستودع R3 جديد ووظيفة نقل](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [ترحيل بند WMSI/WMS2](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [ترقية إدارة المستودعات من Microsoft Dynamics AX 2012 to Supply Chain Management](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]