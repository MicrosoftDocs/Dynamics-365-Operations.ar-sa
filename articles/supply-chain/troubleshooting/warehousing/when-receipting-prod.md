---
title: تتم طباعة تسمية واحدة فقط لرؤوس العمل المتعددة في إيصال واحد
description: تتم طباعة تسمية واحدة فقط لرؤوس العمل المتعددة في إيصال واحد.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026234"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="d9020-103">تتم طباعة تسمية واحدة فقط لرؤوس العمل المتعددة في إيصال واحد</span><span class="sxs-lookup"><span data-stu-id="d9020-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="d9020-104">رقم KB: 4614667</span><span class="sxs-lookup"><span data-stu-id="d9020-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="d9020-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="d9020-105">Symptoms</span></span>

<span data-ttu-id="d9020-106">يتم إنشاء العديد من رؤوس العمل لنفس لوحة الترخيص الهدف كجزء من حدث استلام تطبيق مستودع واحد.</span><span class="sxs-lookup"><span data-stu-id="d9020-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="d9020-107">ومع ذلك، تتم طباعة تسمية واحدة فقط من لوحات التراخيص عند استلام المنتج.</span><span class="sxs-lookup"><span data-stu-id="d9020-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="d9020-108">الدقة</span><span class="sxs-lookup"><span data-stu-id="d9020-108">Resolution</span></span>

<span data-ttu-id="d9020-109">يعمل النظام كما هو مصمم.</span><span class="sxs-lookup"><span data-stu-id="d9020-109">The system is behaving as designed.</span></span>

<span data-ttu-id="d9020-110">في التصميم الحالي، يتم دائمًا إنشاء تسمية لوحة ترخيص واحدة، بغض النظر عن عدد مجموعات أسطر العمل ورأس العمل الموجودة.</span><span class="sxs-lookup"><span data-stu-id="d9020-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="d9020-111">تتضمن التسمية التي تم إنشاؤها المعلومات الخاصة بمجموعة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="d9020-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="d9020-112">لحل هذه المشكلة، تأكد من تعيين رأس العمل دائمًا إلى لوحة ترخيص هدف واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="d9020-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
