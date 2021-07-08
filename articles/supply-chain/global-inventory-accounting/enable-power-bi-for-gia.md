---
title: تمكين Power BI لمحاسبة المخزون العالمي
description: يصف هذا الموضوع كيفية تمكين Microsoft Power BI لمحاسبة المخزون العالمي.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273107"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>تمكين Power BI لمحاسبة المخزون العالمي

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

يمكنك تثبيت الإطارات المتجانبة ولوحات المعلومات والتقارير من حساب [PowerBI.com](https://powerbi.com/) الخاص بك إلى مساحة عمل تطبيق Microsoft Dynamics 365 .

## <a name="prerequisites"></a>المتطلبات الأساسية

يجب أن تكون المتطلبات الأساسية التالية في مكانها قبل تمكين تقارير Power BI:

- يجب أن تكون مسؤول نظام في تطبيق Dynamics 365.
- يجب أن يكون لديك حساب [PowerBI.com](https://powerbi.com/).
- يجب أن يكون لديك لوحة معلومات واحدة وتقرير واحد على الأقل في حساب Power BI الخاص بك.
- يجب أن تكون مسؤولاً عن حساب Azure Active Directory (Azure AD).
- يجب أن يكون المجال Azure AD هو نفس المجال الذي استخدمته لحساب [PowerBI.com](https://powerbi.com/).

## <a name="setup"></a>الإعداد

اتبع الخطوات التالية لإعداد تكامل Power BI.

1. سجل دخولك إلى [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. انتقل إلى **مكتبة الأصول المشتركة**، حدد نموذج التقرير **Power BI**، كنوع الأصل، وقم بتنزيل الحزمة **محاسبة المخزون العالمي**. 
1. قم بتسجيل الدخول إلى [PowerBI.com](https://app.powerbi.com/)، وقم بتحميل ملف تقرير **محاسبة المخزون العالمي** Power BI باتباع الخطوات التالية:

    1. حدد **جديد**.
    1. حدد **تحميل ملف**.
    1. حدد ملف التقرير **محاسبة المخزون العالمي** Power BI.

1. قم بتكوين التقرير **محاسبة المخزون العالمي** Power BI باتباع الخطوات التالية:

    1. انتقل إلى **مساحة العمل الخاصة بي**، وابحث عن مجموعة البيانات الخاصة بمحاسبة المخزون العالمي، ثم في القائمة **الخيارات**، حدد **الإعدادات**.
    1. في **إعدادات محاسبة المخزون العالمي**، قم بتوسيع **المعلمات**، وقم بتحديث كل المعلمات كما هو مطلوب.

1. قم بتسجيل التطبيق كما هو موضح في [تكوين تكامل PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).
1. قم بتكامل ملف التقرير **محاسبة المخزون العالمي** Power BI في Dynamics 365 Supply Chain Management باتباع الخطوات التالية:

    1. انتقل إلى **إدارة النظام \> الإعداد \> تكوين PowerBI.com**.
    1. حدد **تحرير**.
    1. حدد **تمكين تكامل PowerBI.Com**.
    1. في الحقل **معرف التطبيق**، أدخل معرف التطبيق:
    1. في الحقل **مفتاح التطبيق**، أدخل مفتاح التطبيق:
    1. حدد **حفظ**.

1. قم بتحديث الصفحة بحيث يظهر مربع حوار تسجيل دخول Power BI.
1. في علامة التبويب **الخيارات**، حدد **فتح كتالوج التقارير**، ثم حدد ملف التقرير **محاسبة المخزون العالمي** Power BI الذي قمت بتحميله مسبقًا.
1. قم بتحديث الصفحة. يجب أن ترى أنه تمت إضافة التقرير الخاص بك.
1. ضمن تقارير **Power BI**، حدد الارتباط **محاسبة المخزون العالمي**.

للحصول على مزيد من المعلومات، راجع [تكوين تكامل PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).
