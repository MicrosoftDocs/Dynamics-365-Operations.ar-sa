---
title: الأصول الواردة والصادرة
description: يشرح هذا الموضوع كيفية تسجيل الأصول الواردة والصادرة في إدارة الأصول.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ee3917725a95d47e37b9c914580e8ce521b52695
ms.sourcegitcommit: 4c8223c9540fbc1c1e554962938058d432e4c681
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/05/2022
ms.locfileid: "8548128"
---
# <a name="inbound-and-outbound-assets"></a>الأصول الواردة والصادرة

[!include [banner](../../includes/banner.md)]

 

إذا كانت شركتك تنفذ مهام إصلاح أو صيانة على أصول تتلقاها من مواقع أخرى أو عملاء أخرين، فبإمكان إدارة الأصول تتبع الأصول الواردة التي هي في طريقها إلى شركتك والأصول الصادرة التي يتم إرجاعها.

> [!NOTE]
> إذا كنت ترغب في استخدام حالات دورة الحياة الواردة والصادرة لإدارة الأصول التي تأتي ويتم إرجاعها، يجب إعداد حالات دورة حياة طلب الصيانة ونماذج دورة الحياة لدعم هذه الإجراءات. لمزيد من المعلومات، راجع [طلبات الصيانة](/d365F-O/supply-chain/asset-management/manage-maintenance-requests/../manage-maintenance-requests/maintenance-request-overview).

يحدد إعداد "إدارة الأصول" ما إذا كان يمكنك العمل مع الأصول الواردة والصادرة.

## <a name="register-assets-as-inbound"></a>تسجيل الأصول كواردة

1. حدد **إدارة الأصول** \> **عام** \> **طلبات الصيانة** \> **طلبات الصيانة النشطة**.
2. حدد طلب الصيانة.
3. حدد **تحديث حالة طلب الصيانة**.
4. حدد **وارد** (أو حالة دورة حياة أخرى قمت بإنشائها للأصول الواردة)، ثم حدد **موافق**.

![تسجيل الأصول كواردة.](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>تسجيل الأصول الواردة كمستلمة

1. حدد **إدارة الأصول** \> **عام** \> **وارد/صادر** \> **الأصول الواردة**.
2. حدد الأصل أو طلب الصيانة.
3. حدد **استلام الأصول**.
4. في الحقل **مُستَلم‬**، أدخل التاريخ والوقت. ثم حدد **موافق**. يُزال السجل من صفحة‏‎ قائمة **الأصول الواردة**.

![تسجيل الأصول الواردة كمستلمة.](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>تسجيل الأصول كصادرة

عند الانتهاء من مهمة الصيانة أو الإصلاح، يمكنك تسجيل الأصل كمرتجع.

1. حدد **إدارة الأصول** \> **عام** \> **طلبات الصيانة** \> **طلبات الصيانة النشطة**.
2. حدد طلب الصيانة.
3. حدد **تحديث حالة طلب الصيانة**.
4. حدد **صادر** (أو حالة دورة حياة أخرى قمت بإنشائها للأصول الصادرة)، ثم حدد **موافق**.

## <a name="register-outbound-assets-as-delivered"></a>تسجيل الأصول كمسلَّمة‬

1. حدد **إدارة الأصول** \> **عام** \> **وارد/صادر** \> **الأصول الصادرة**.
2. حدد الأصل أو طلب الصيانة.
3. حدد **تسليم الأصول**.
4. في الحقل **مسلَّمة‬**، أدخل التاريخ والوقت. ثم حدد **موافق**. يُزال السجل من صفحة‏‎ قائمة **الأصول الصادرة**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]