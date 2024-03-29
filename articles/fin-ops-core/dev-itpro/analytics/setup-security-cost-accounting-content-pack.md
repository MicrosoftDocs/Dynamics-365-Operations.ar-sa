---
title: إعداد الأمان لمحتوى Power BI لتحليل محاسبة التكاليف
description: توضح هذه المقالة كيفية نشر مستوى الوصول الآمن في محاسبة التكاليف إلى الأمان على مستوى الصف في Microsoft Power BI.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.openlocfilehash: 9f019bec9c28602e31b43a8b3ab820f4a3a31ee8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267921"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>إعداد الأمان لمحتوى Power BI لتحليل محاسبة التكاليف

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية نشر مستوى الوصول الآمن في محاسبة التكاليف إلى الأمان على مستوى الصف في Microsoft Power BI. تضمن هذه الوظيفة ألا يشاهد المستخدم سوى بيانات Power BI التي مُنح إمكانية الوصول لها.

## <a name="overview"></a>نظرة عامة

يستخدم محتوى **تحليل محاسبة التكاليف** في Microsoft Power BI الأمان على مستوى الصف في Power BI لتقييد وصول المستخدم. يستند الأمان على التدرج الهرمي المؤسسي لمستوى الوصول الذي تم إعداده في معلمات محاسبة التكاليف. لمزيد من المعلومات حول محتوى **تحليل محاسبة التكاليف** في Power BI، راجع [محتوى "تحليل محاسبة التكاليف" في Power BI](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>الإعداد
لنشر مستوى الوصول الآمن إلى Power BI، يجب على مالك محتوى Power BI اتباع الخطوات التالية.

> [!NOTE]
> يصبح المستخدم الذي ينشر محتوى **تحليل محاسبة التكاليف** في Power BI مالك المحتوى بشكل تلقائي. بإمكان المالك فقط إعداد الأمان في Power BI. بالإضافة إلى ذلك، وحتى قيام المالك بإضافة مستخدمين على PowerBI.com، لا يمكن لأي شخص بخلاف المالك رؤية أي بيانات في محتوى **تحليل محاسبة التكاليف** في Power BI.

1. نشر ملف التعريف إلى Power BI.
2. تسجيل الدخول إلى PowerBI.com.
3. العثور على قاعدة بيانات **تحليل محاسبة التكاليف** في Power BI.
4. فتح صفحة الأمان.

    ![فتح صفحة الأمان.](./media/CA-picture-1.png)

5. **مراقب كائن التكلفة** قد تم إنشاؤه بالفعل. إضافة أعضاء آخرين يشكلوا جزءًا من التدرج الهرمي المؤسسي لمستوى الوصول لمحاسبة التكاليف.

    ![إضافة الأعضاء.](./media/CA-picture-2.png)

سوف يرى المستخدمون الذين تم إضافتهم إلى دور **مراقب كائن التكلفة** البيانات المسموح لهم برؤيتها فقط، وفقًا للتعريف في التدرج الهرمي المؤسسي لمستوى الوصول لمحاسبة التكاليف.

> [!NOTE]
> ينطبق الأمان على مستوى الصف على الإطارات المتجانبة والتقارير في المضمنة من Power BI.

## <a name="updating-security"></a>تحديث الأمان
إذا تم تحديث الأمان على مستوى الوصول في محاسبة التكليف، وأردت أن يعكس Power BI هذه التحديثات، فعليك تحديث مخزن الكيانات لمحتوى **تحليل محاسبة التكاليف** في Power BI. بعد الانتهاء من تحديث متجر الكيان، يجب عليك تحديث المنتجات على PowerBI.com. لمزيد من المعلومات حول كيفية تحديث متجر الكيان، راجع [تكامل Power BI مع مخزن الكيانات](power-bi-integration-entity-store.md#update-entity-store). يتعين أيضًا على مالك محتوى **تحليل محاسبة التكاليف** في Power BI إجراء تحديث لمخزن الكيانات إذا تم منح مستخدمين جدد إمكانية الوصول إلى التدرج الهرمي للمؤسسات. بالإضافة إلى ذلك، يجب على المالك إضافة مستخدمين جدد إلى دور **مراقب كائن التكلفة** في PowerBI.com، حيث يتم تطبيق الأمان على مستوى الصفوف لها.

## <a name="disabling-security"></a>تعطيل الأمان
نفترض أن مؤسستك ترغب في تقييد الوصول إلى البيانات. إذا تم تعطيل معلمات الأمان، لسبب ما، عند تشغيل محاسبة التكاليف، فيجب على المالك إضافة دور **محاسب التكاليف** في Power BI بدلًا من ذلك. إذا قمت بتغيير الأمان من حالة التمكين إلى حالة التعطيل، فمن المستحسن إزالة مستخدمين من دور **مراقب كائن التكلفة**. والعكس بالعكس إذا كنت تقوم بإعادة تمكين الأمان. يمكن للمستخدمين الانتماء إلى كلا الدورين. يمثل الوصول المشترك اتحاد كل من الدورين. وفيما يتعلق بمحتوى **تحليل محاسبة التكاليف** في Power BI، سيتمكن المستخدمون الذين لديهم حق وصول مشترك باكتساب حق وصول غير مقيد إلى البيانات. إذا كان الهدف تطبيق الوصول المقيد، يجب تعيين المستخدمين فقط على دور **مراقب كائن التكلفة**. تسري تحديثات الأمان على مستوى الصف فورًا. يجب على المستخدمين المتأثرين تحديث مستعرضاتهم.

## <a name="additional-resources"></a>الموارد الإضافية
لمزيد من المعلومات حول الأمان على مستوى الصف في Power BI، راجع [إدارة الأمان على النموذج في Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
