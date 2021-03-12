---
title: استكشاف أخطاء عروض أسعار المبيعات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع عروض أسعار المبيعات.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 98011dbf22ff55b7651ce63557fa4a360130b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974750"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="5d4d6-103">استكشاف أخطاء عروض أسعار المبيعات وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="5d4d6-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="5d4d6-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع عروض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="5d4d6-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="5d4d6-105">لا يمكنني تغيير كمية المبيعات لعرض أسعار المبيعات لصنف خدمة.</span><span class="sxs-lookup"><span data-stu-id="5d4d6-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d4d6-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="5d4d6-106">Issue description</span></span>

<span data-ttu-id="5d4d6-107">إذا حاولت تعيين كمية مبيعات (الحقل **SalesQty**) لصنف من النوع *خدمة* على بند عرض أسعار مبيعات، ستتلقى الرسالة التالية: "التحديث غير مسموح لحقل الكمية."</span><span class="sxs-lookup"><span data-stu-id="5d4d6-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5d4d6-108">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="5d4d6-108">Issue resolution</span></span>

<span data-ttu-id="5d4d6-109">لا يمكنك تعيين كمية مبيعات للمنتجات التي تعد أصناف خدمة.</span><span class="sxs-lookup"><span data-stu-id="5d4d6-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="5d4d6-110">على سبيل المثال، إذا قمت بتقديم خدمة لتثبيت صنف، فلا يكون هذا الأمر منطقيًا لتسجيل كمية، بسبب عدم وجود صنف فعلي.</span><span class="sxs-lookup"><span data-stu-id="5d4d6-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="5d4d6-111">توجد خدمة فقط.</span><span class="sxs-lookup"><span data-stu-id="5d4d6-111">There is only a service.</span></span>

