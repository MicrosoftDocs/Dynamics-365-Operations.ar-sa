---
title: الأصول الواردة والصادرة
description: يشرح هذا المقال كيفية تسجيل الأصول الواردة والصادرة في إدارة الأصول.
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
ms.openlocfilehash: e0c382efda81067ad4c0cd977e5cfbf37b4e3fc6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908703"
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