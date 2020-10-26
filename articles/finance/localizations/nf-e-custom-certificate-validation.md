---
title: التحقق من صحة الشهادة NF-e مخصصة
description: يوفر هذا الموضوع معلومات حول تمكين شهادة NF-e مخصصة واستخدامها.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 3c88c4adafb78b807842b0b41c69b19cf2b7aa23
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973082"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="c9573-103">التحقق من صحة الشهادة NF-e مخصصة</span><span class="sxs-lookup"><span data-stu-id="c9573-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9573-104">عند تشغيل ميزه التحقق من صحة شهادة NF-e مخصصة، يسمح التحقق المخصص من الصحة بالاتصال بخدمات الويب.</span><span class="sxs-lookup"><span data-stu-id="c9573-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="c9573-105">هذا الاتصال مطلوب لإرسال NF-e واستلام التخويل من SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="c9573-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="c9573-106">يتم إصدار خاصيه **غرض مصادقه الخادم** من الشهادة V5 من قبل هيئه Brazilian Root Certificate Authority.</span><span class="sxs-lookup"><span data-stu-id="c9573-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="c9573-107">يتم إيقاف تشغيل هذه الخاصية افتراضيا ويجب تمكينها يدويا.</span><span class="sxs-lookup"><span data-stu-id="c9573-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="c9573-108">في بعض الحالات، يمكن لتحديث الشهادة التلقائي تبديل هذه الخاصية إلى لم يعد ممكنا.</span><span class="sxs-lookup"><span data-stu-id="c9573-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="c9573-109">إذا حدث ذلك، فان اتصال TLS متأثر ولا يعد موثوقا به.</span><span class="sxs-lookup"><span data-stu-id="c9573-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="c9573-110">وتتاثر القدرة علي إصدار NF-e في بيئات الإنتاج لولايات ميناس جريس (MG) وولايات بارانا (PR) أيضا.</span><span class="sxs-lookup"><span data-stu-id="c9573-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="c9573-111">يسمح هذا التحديث بحل بديل للتحقق من صحة الشهادة، مما يعني انه من الممكن تاسيس اتصال آمن.</span><span class="sxs-lookup"><span data-stu-id="c9573-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


