---
title: "الوصول إلى العناوين الخاصة حسب دور الأمان"
description: "يتناول هذا الموضوع كيفية حل هذه المشكلة والتي يتعذر فيها على العميل الوصول إلى عناوين خاصة."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.contentlocale: ar-sa
ms.lasthandoff: 12/04/2018

---

# <a name="access-to-private-addresses-by-security-role"></a>الوصول إلى العناوين الخاصة حسب دور الأمان

[!include [banner](includes/banner.md)]

**المشكلة**

بعد تكرار العميل لدور أمان وتسجيل الدخول بهذا الدور الجديد، فلا يمكن للعميل الاطلاع على العناوين التي تم وضع علامة "خاص" عليها.

**‏‏الدقة**

لحل هذه المشكلة، يجب على العميل اتباع الخطوات التالية لدور الأمان المُكرر.

1. انتقل **إدارة المؤسسة \> دفتر العناوين العمومي \> محددات دفتر العناوين العمومية**.
2. في علامة تبويب **أمان الموقع الخاص**، قم بنقل دور الأمان الجديد من قائمة **الأدوار المتاحة** إلى قائمة **الأدوار المُحددة**.
3. حدد **حفظ**.

![صفحة محددات دفتر عناوين عمومي](media/GAD-parameters.png)

